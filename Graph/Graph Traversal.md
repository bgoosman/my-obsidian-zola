[[Graph]]
# General Traversal Algorithm

**tricolor algorithm**

* **White** nodes are undiscovered nodes that have not been seen yet in the current traversal and may even be unreachable.
* **Black** nodes are reachable nodes that the algorithm has already visited and is finished processing.
* **Gray** nodes are nodes that have been discovered but that the algorithm is still processing. These nodes are on the frontier between white and black.

tricolor invariant
1\. The root is not white.
2\. There is no edge from a black node to a white node.

tricolor pseudo-code
```
Color the root node gray and all other nodes white;
while some gray node n exists:
  color some white successors of n gray;
  if n has no white successors, optionally color n black.
```

# Traversal Algorithms

options

* directional = {true, false}
* neighborCompareFn
  * for bfs, defines order neighbors appear in the queue
  * for dfs, defines order neighbors are traversed
  * (left, right) = -1 if left<right, 0 if left==right, 1 if left>right
  * e.g. findNeighbors(node, {directional}).sort(neighborSort)
* visitFn = (graph, node, neighbors)
* visitOrder (only for DFS)
  * preorder (visit node, then neighbors)
  * inorder (if 2 neighbors, then dfs(first), visit(node), dfs(second). Otherwise, use postorder)
  * postorder (dfs(neighbors), visit node)

bfs

* complexity
  * space = O(V) e.g. (max degree)^2
  * time = O(V)
* globals
  * queue
* input
  * graph
  * root
  * options
* output
  * visited nodes and edges
  * node distance from root

```
function bfs({graph, root, directed}) {
  const nodeDistance = new Map();
  const visitedNode = new Map();
  visitNodeFn(graph, root);
  visitedNode.set(root.id, true);
  nodeDistance.set(root.id, 0);
  let distance = 1;
  let queue = graph.findNeighbors(root.id, { directed });
  while (queue.length > 0) {
    let nextQueue = [];
    queue.forEach(({ connectedEdge, neighbor }) => {
      if (!visitedEdge.has(connectedEdge.id)) {
        visitEdgeFn(graph, connectedEdge);
      }
      const {id: neighborId} = neighbor;
      if (!visitedNode.has(neighborId)) {
        visitNodeFn(graph, neighbor);
        visitedNode.set(neighborId, true);
        nodeDistance.set(neighborId, distance);
        nextQueue = nextQueue.concat(
          graph.findNeighbors(neighborId, { directed })
        );
      }
    });
    queue = nextQueue;
    distance++;
  }
  return {
    visitedNode,
    visitedEdge,
    nodeDistance,
  }
}
```
dfs

* complexity
  * space = O(V) e.g. max depth
  * time = O(V)
* input
  * graph
  * root
  * options
* output
  * visited nodes and edges
  * visited order

# Applications of Traversal Algorithms

findReachableSubgraph
```
const subgraph = api.makeGraph()
bfs({
  directional: true,
  visitNodeFn: ({node}) => subgraph.addNode(node),
  visitEdgeFn: ({edge}) => subgraph.addEdge(edge),
  root,
});
return subgraph;
```
doesCycleExist
```
const state = dfs({
  directed: true,
  root,
})
return state.hasEdgeType('BACK_EDGE')
```
topologicalSort
```
const totalOrder = [];
let state;
for (const root of graph.getNodes()) {
  if (state?.isNodeVisited(root))
    continue;
  state = dfs({
    directional: true,
    visitNodeFn: ({node}) => totalOrder.push(node),
    visitOrder: 'preorder',
    root,
    state,
  });
}
return totalOrder
```

* requires DFS
* input
  * graph
* output
  * node order
* algorithm
  * globals
    * order
  * while there are unvisited nodes, dfs(whiteNodes.pop())
  * visit(node) => set node order = order++

# Sources

* http://www.cs.cornell.edu/courses/cs2112/2018fa/lectures/lec\_traversals/

    Created at: 2022-07-08
    Updated at: 2022-07-08

