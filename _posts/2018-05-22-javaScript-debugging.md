---
layout: post
title: JavaScript Debugging
---

Programming is a constant cycle of coding - debugging - fixing. To be a great programmer it's not enough to be good at programming language, but also to be good at mastering the art of debugging failures.

This article helps in understanding the debug approach and gives an overview of the tools that assist you in your debug cycle.

* **Identify the issue - What is actually happening vs what you expect to happen.**
  
The very first step in debugging is identifying the problem. Problems could be error messages (like syntax error, undefined variables etc.), wrong behaviour of the code (like a add function giving wrong output etc.) or nothing is happening (like you click a button and nothing happens etc.)

To take an example and explore it further, say if a click action on a button results in a success message or an error message, if we see that none of this happens and really nothing changes, we know that something is not right!  We understand that there is some issue with the button and its associated logic. 

The next step would be to completely understand when this failure occurs and under what circumstances this condition gets created.

* **Reproduce - Outline exact reproduction steps.** 

We should be able to reproduce the failing condition to actually debug it! 

Questions to ask are, is this behavior happening only when a certain sequence of steps are followed? Is it happening all the time? Is it occuring only in production code and not in your development environment? 

Once we understand the sequence of steps or the conditions that lead to this behavior, we are in a position to go look into the code and start debugging where exactly the code is failing! 

* **Isolate - Where exactly the bug is in your code.**

Now we start to narrow down exactly where inside the code the failure occurs! JavaScript has debugging features like the console object and debugger statements that help us print out information on the browser console to get a better understanding of our code stack and trace the flow of our program.

Below is a list of few console methods. Mozilla’s developer documentation site is a great place to get deeper understanding of these methods.

console.log() - Helpful to log general information

console.error() - Helpful in throwing error messages

console.trace() - Shows you the stack trace, path followed to reach the point where the trace() was called.

**Chrome browser’s Chrome Developer tool** is a very helpful tool to inspect your html, css and javaScript code. It lets you edit the code in the browser and then reflects those changes on your web page which totally speeds up your debug cycle. Thing to remember here is that the changes to the code in the browser don’t change the code in your database so a refresh to the page will result in changes lost. It essentially lets you see all your console messages, lets you edit your code, helps in inspecting every element and tag in your code and provides information related to network errors.

**Debugger statement** in javaScript is another great feature which lets you set up breakpoints in your program so you can slow down the code execution. You can then step through the code execution to see the changes happening in your local variables. 

**Lint** is great to help you clean out any code syntax errors. The error messages thrown out by lint are more clear and help speed up the debugging process.

**Pair programming** Once you have spent some time debugging and say you are stuck, don’t shy away from taking help from your peers! Pair programming helps you see things that you might have missed. Gist is a great tool to share your code snippet with peers for discussion and feedback. 

Use [Mozilla](https://developer.mozilla.org/en-US/docs/Web) and [stackoverflow](https://stackoverflow.com/) websites to assist you in your debug. Sometimes simply typing the error message in google can give you immediate answers to the cause of the failure.

Having tracked down the lines of code which resulted in the failing condition, it's time to fix it!

* **Solve - Understand why the failure happened and fix it.**

Once you have debugged and narrowed down the cause of the failure, fix it and test it to make sure the bug is fixed and the code is behaving as expected. Add a testcase to the test suite to capture the sequence that led to this bug.

Sharing the learnings with others in the team is a good idea since it will prevent others from making similar mistakes.

Here’s wishing you Happy Debugging!!!
