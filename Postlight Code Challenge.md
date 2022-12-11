
## Full Stack Engineer Code Challenge

Thanks for interviewing at Postlight as a Full Stack Engineer. We’re asking you to complete this take-home code challenge so that we can better understand your technical skills. Expect to spend up to 8 hours working on this challenge, as your schedule allows. Let us know if you cannot complete the challenge within a week. Be creative, and have fun! If you have any questions about this challenge, feel free to reach out. Reply to the original email in which you received this challenge and we will get back to you as soon as we can (within a couple of business days).

Frontend

* Bundling: [snowpack](https://www.snowpack.dev/#unbundled-development) came out in [2019 replaces webpack as a code bundler](https://blog.logrocket.com/snowpack-vs-webpack/)
* Next-gen JS: [babel](https://babeljs.io/)
* CSS in JS: [astroturf](https://github.com/4Catalyzer/astroturf)
* CSS preprocessor: [PostCSS](https://github.com/postcss/postcss#usage) can do everything Sass can and more 
* CSS utility classes: [tailwind](https://tailwindcss.com/) via PostCSS. [VS Code plugin](https://marketplace.visualstudio.com/items?itemName=bradlc.vscode-tailwindcss)
* UI framework: There are so many of these. I’ve used Material UI before but am open to a change. [Most accessible frameworks.](https://darekkay.com/blog/accessible-ui-frameworks/) [React Bootstrap](https://react-bootstrap.github.io/getting-started/introduction). [Reddit 1](https://www.reddit.com/r/reactjs/comments/ba8pxp/react_question_which_ui_framework_to_choose/)
* Grid layout: [React Grid Layout](https://github.com/STRML/react-grid-layout)
* View framework: React
* JavaScript runtime: Node
* Animation: [Framer Motion](https://www.framer.com/motion/) EDIT: [OMG I'M IN LOVE WITH A LIBRARY](https://www.reddit.com/r/reactjs/comments/cbin51/framer_motion_the_successor_to_pose_by_popmotion/etfzin6?utm_source=share&utm_medium=web2x&context=3)

```
<motion.div
animate={{

x: 26,

y: -84,

scale: 0.5,

rotate: 86,
}}
/>
```

* TypeScript or JavaScript: JavaScript. Faster to prototype w/out types + haven’t written a whole app in JS, since I started with TS at Expedia.
* Testing: Jest, [react-testing-library](https://github.com/testing-library/react-testing-library)

Backend

* Web framework: expressjs
* IaC: serverless
* Logging with default loglevel
* Database: PostreSQL (because Heroku has a free db)
* API: GraphQL (graphql-yoga?)
  * Filtering by department, title, location

Requirements

* List employees
* Filter by 

Design

* <https://www.quora.com/What-are-the-best-UX-UI-design-patterns-for-internal-employee-directories-e-g-search-for-colleagues-throughout-an-organization-with-different-criteria>

Features

* sessions

### The Task

* Employee directory web application
* Front and back end
* Using modern tools like GraphQL or JSON API
* Include names, pictures, job titles, and anything else you see fit.
* Code quality
* Readability.
* Production quality

**We don’t expect you to complete every suggested feature below.**

#### Suggested Features

* README.md
* Developer diary
* React
* Node
* Filter employees by department, title, location
* Use of a client-side router i.e. react-router-dom
* Creative use of animation.
  * Sidebar that opens and closes
  * <https://github.com/FormidableLabs/react-animations> tada to drop attention
* Paginated lists.
* Forms for creating, updating, and deleting employees.
* Source data from a third party person API, such as [https://randomuser.me](https://randomuser.me/) or [http://uifaces.com](http://uifaces.com/).
* Ability to search for employees.
* Testing.

### What We’re Not Looking For

We don’t expect your visual design to be perfectly polished. We’re more interested in your implementation than your design. It’s okay and encouraged to use existing libraries and frameworks. We know you will be missing assets you would include in a production environment (like icons and logos). Skip those and document what would be more complete in your project in a production environment.

### Delivery

Once complete, please reply to the original email with your submission. We encourage you to include a git repository with history, excluding any files you would typically leave uncommitted (such as your node\_modules folder). If you need more time, we understand -- just let us know.
Please submit here:
<https://app2.greenhouse.io/tests/96de8e254b354ff0111cbf8df619f513?utm_medium=email&utm_source=TakeHomeTest>

2020-09-01

* Install Snowpack, Node, React, Framer Motion PostCSS, tailwindcss, astroturf
* Goals: Set up the stack online. Audit DynamoDB costs

    Created at: 2020-08-29
    Updated at: 2020-09-04

