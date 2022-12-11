[[Clean Code]]
* Should do one thing. So, another way to know that a function is doing more than “one thing” is if you can extract another function from it with a name that is not merely a restatement of its imple- mentation.
* Cannot be divided into sections.
* Has on level of abstraction. e.g. Don’t mix “getHtml()” with "String pagePathName = PathParser.render(pagePath);"
* Are organized top down in level of abstraction.
* If a function accepts a boolean, consider splitting it into two functions.
* Has no side effects

Switch statements can be replaced by polymorphism and AbstractFactory.

    Created at: 2020-03-28
    Updated at: 2020-03-28

