---
layout: post
title: Ruby Debugging
---
This article helps in understanding the debug approach and gives an overview of the tools that assist you in debugging ruby code.

* Identify the issue - What is actually happening vs what you expect to happen.
  
The very first step in debugging is identifying the problem. Problems could be error messages (like syntax error, undefined variables etc.), wrong behaviour of the code (like a add function giving wrong output etc.) or there is nothing happening (like you click a button and nothing happens etc.)

To take an example and explore it further, say if a click action on a button results in a success message or an error message, if we see that none of this happens and really nothing changes, we know that something is not right!  We understand that there is some issue with the button and its associated logic. 

The next step would be to completely understand when this failure occurs and under what circumstances this condition gets created.

* Reproduce - Outline exact reproduction steps. 

We should be able to reproduce the failing condition to actually debug it! 

Questions to ask are, is this behavior happening only when a certain sequence of steps are followed? Is it happening all the time? Is it occuring only in production code and not in your development environment? 

Once we understand the sequence of steps or the conditions that lead to this behavior, we are in a position to go look into the code and start debugging where exactly the code is failing! 

* Isolate - Where exactly the bug is in your code.

Now we start to narrow down exactly where inside the code the failure occurs! 

Putting print/puts/p statements inside your ruby code to trace the flow of your program is very helpful. You can also print out variables to get better insight into your code.


**IRB (Interactive Ruby Shell)** - IRB is very helpful when you want to execute ruby commands on the fly.

You could copy/paste snippets of your code to test ruby methods locally so as to narrow down the problem in your code. You can also “require” your code in irb shell instead of pasting it and call the ruby methods from the shell to see the behavior of your code. IRB also provides line numbers when throwing up the error so that helps in exactly knowing which line of code gave the error. 

**Pry** - Pry is a great tool for debugging your code. 

You can put a breakpoint in your code to stop the program execution. You put “binding.pry” statement inside your method where you want the program execution to stop. You can then inspect your variables and continue the execution step by step using the “continue” command on the pry command prompt. 

**Exceptions** - When a program raises an exception, it can crash the application.

By anticipating the possibility of an operation causing an error, we can wrap it up in a rescue block. For instance if you don’t want to restrict a user from giving any input to your application, then take care of that invalid input by adding a rescue block which handles the invalid entry and thereby preventing the application from crashing.

Above were some of the ways to help debug a failing ruby code. Having tracked down the lines of code which resulted in the failing condition, it's time to fix it!

* Solve - Understand why the failure happened and fix it. 

Once you have debugged and narrowed down the cause of the failure, fix it and test it to make sure the bug is fixed and the code is behaving as expected. Add a testcase to the test suite to capture the sequence that led to this bug.

Once fixed, it would do good to share the learnings with others.

Here’s wishing you Happy Debugging!!!
