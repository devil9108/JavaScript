# 2020 JS New Features

## globalThis

To get the window object we use `window` or `this` in the JS which referse to the window Object.

**Different Ways to get Window Object**

```
console.log(window);
console.log(self); //if we use webworker self works
console.log(frames);
console.log(this); //this will return window if we use in global scope
```

In NodeJs we cant use window for the global object we have to use global there.

To make unique through all the platforms they introduced _globalThis_ to get the global Object.

## Promise.allSettled()

To know all the promises are completed or not we can use `Promise.allSettled([promises]);`. Default we have Promise.all to know all the promiseses are done or not. But that will retrun if all promises are resolve. By using allSettled we can get weither some get reject and some get resolve also.

# Execution Context

Execution Context is an environment where the javascript code runs and executes.

## Types of Execution Contexts

1. **Global Execution Context -->**
   This is the main exection context in javascript. The code which is recides out of any function is comes under global exection context. It creates the Window Object(global object). And it sets the `this` value equal to Global Object.

2. **Functional Execution Context -->**
   Everytime function invoked, new exectuin context for that function is created. Which is called Functional Exectuin Context. There can be any nuber of Functional Execution Context. Each function has its own execution context, but its created when it is invoked or called.
3. **Eval Function Execution Context -->**
   Code executed inside an eval function also gets its own execution context, but as eval isn’t usually used by JavaScript developers.

# Execution Stack

![Image](/images/execution-stack.png)
