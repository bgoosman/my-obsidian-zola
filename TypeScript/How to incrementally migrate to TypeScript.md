[[TypeScript]]
https://www.reddit.com/r/typescript/comments/u9g6f2/should_a_team_of_one_me_with_some_ts_experience/

```
You can incrementally migrate to ts. You just change all your JS files to ts extension and setup webpack with a ts-loader step. Then set your tsconfig.json to allow relatively permissive typing of any and you'll be good to go. From there you can incrementally add static typing to features & start leveraging ts language features.
```

```
I had good results doing the same thing 1.5 years ago at my company. We had good luck with using AirBNBs typescript converter. Its not perfect but does a lot of the lifting for you (renaming files etc). Totally worth it. Good luck
```
- [https://github.com/airbnb/ts-migrate](https://github.com/airbnb/ts-migrate)

```
Whether you should do it _now_ is a question of time and priorities. However, as a general thing: yes, I _highly_ recommend trying to get app code into TS as soon as possible.

FWIW I have some tips on migrating code to TS here (along with war stories of migrating a real AngularJS1 + Express app to TS):


Related, the canonical resource for using React + TS together is this site:

```
- [https://blog.isquaredsoftware.com/2021/12/codebase-conversion-mean-react-next-ts/#typescript-file-conversion-approach-and-techniques](https://blog.isquaredsoftware.com/2021/12/codebase-conversion-mean-react-next-ts/#typescript-file-conversion-approach-and-techniques)
- [https://react-typescript-cheatsheet.netlify.app/](https://react-typescript-cheatsheet.netlify.app/)

```
	Loads of good advice here. To add, if you think about it intelligently, there’s often a lot less work to do than you’d think. If you type all the places where data comes into your system - usually api responses, maybe some user input - then converting the files that import these and so on, you will find that a lot of the work is done for you just through inference 
```