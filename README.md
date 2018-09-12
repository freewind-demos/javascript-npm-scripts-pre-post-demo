JavaScript Npm "pre" "post" Demo
================================

假设在npm的"scripts"里有一条命令`demo`，希望在执行它的前后，同时执行一些别的命令，怎么办？

可以再定义两条命令，分别在前面加上`pre`即可，即`predemo`和`postdemo`。

这样我们在执行`npm run demo`的时候，`predemo`和`postdemo`会在它前后分别执行。

```
npm install
npm run demo
```

You will see:

```
> @ predemo /Users/freewind/workspace/javascript-npm-scripts-pre-post-demo
> echo --- predemo ---

--- predemo ---

> @ demo /Users/freewind/workspace/javascript-npm-scripts-pre-post-demo
> node hello.js

Hello, NPM

> @ postdemo /Users/freewind/workspace/javascript-npm-scripts-pre-post-demo
> echo --- postdemo ---

--- postdemo ---

```
