[[JavaScript]]
RxJS producers can signal to consumers that there is no more data -> onCompleted and there is an error -> onError. i.e. exceptions not needed

RxJS pipes can accept promise returning functions
<https://benlesh.medium.com/rxjs-observable-interop-with-promises-and-async-await-bebb05306875>

RxJS stream to [async iterable](https://developer.mozilla.org/en-US/docs/Web/JavaScript/Reference/Global_Objects/Symbol/asyncIterator)
<https://www.npmjs.com/package/rxjs-for-await>
<https://indepth.dev/posts/1196/rxjs-for-await-what>
```
async function example() {
  const source$ = interval(100);

  for await (const value of eachValueFrom(source$)) {
    console.log(value);
  }
}
```
Could use this for finding lesions on app startup. Turn findLesion into a stream

* eachValueFrom
* bufferedValuesFrom
* latestValuesFrom
* nextValueFrom

# Operators

* finalize, executes when stream completes or errors

# Nesting streams with switch/merge/concat/exhaustMap

These functions flatten the output of the nested stream

* switchMap cancels the prior output of the nested stream when a new input comes in (e.g. good for READ events) (i.e. sort of like throttle)
* mergeMap takes all the outputs of the nested stream, in any order (e.g. good for WRITE events)
* concatMap is like mergeMap but it flattens in the order of the input stream (safest for WRITE events)
* exhaustMap takes the first event and ignores any pending events, then processes the next event after the first event completes

<https://ncjamieson.com/avoiding-switchmap-related-bugs/>

* use `concatMap` with actions that should be neither aborted nor ignored and for which the ordering must be preserved — it’s also a conservative choice that will always behave in a predictable manner;
* use `mergeMap` with actions that should be neither aborted nor ignored and for which the ordering is unimportant;
* use `switchMap` with read actions that should be aborted when another action of the same type is dispatched; and
* use `exhaustMap` with actions that should be ignored whilst an action of the same type is pending.

# redux-observable

redux-observable maps user intent actions to state transfer actions
e.g. REMOVE\_FROM\_CART -> \*async operations / side fx\* -> REMOVE\_FROM\_CART\_FULFILLED

# RxJS stream -> React re-render

<https://dev.to/rxjs/fetching-data-in-react-with-rxjs-and-lt-gt-fragment-54h7>
<https://github.com/LeetCode-OpenSource/rxjs-hooks>

* useObservable (observable -> value)
* useEventCallback (component event prop -> observable -> state)

Alternative to ^ <https://github.com/crimx/observable-hooks>

# Combine streams into computed values that re-compute when the streams emit

<https://github.com/kosich/rxjs-autorun>    

# RxJS and React hooks

<https://nils-mehlhorn.de/posts/react-hooks-rxjs>

# RxJS and fetch

<https://www.learnrxjs.io/learn-rxjs/operators/creation/ajax>

# Pagination example

<https://github.com/nilsmehlhorn/react-rxjs-pagination-example/blob/master/src/lib/pagination.ts>
Pipe

* params (sort, query)
  * switchMap pageNumber (start with 0)
    * switchMap endpoint(page, sort, size, query) ->

    Created at: 2022-09-02
    Updated at: 2022-09-02

