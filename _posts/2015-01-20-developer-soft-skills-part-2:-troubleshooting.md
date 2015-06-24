---
layout: post
title: Developer Soft Skills Part 2 - Troubleshooting
cover:
date:   2015-06-30 12:00:00
categories: posts
---

#Developer Soft Skills Part 2: Troubleshooting

This part of the Developer soft skills is about finding and solving an issue. Most often in development these issues are referred to as bugs. Knowing which tools to use, where to look and how to squash a bug would allow a developer to spend less time fixing things. That gives us more time to make better code, develop new features and work on other projects. Or even more time to spend doing things that don't involve code (I know some people that actually do that).

##Finding the issue
![Seraching](/images/blog/searching.jpg "Searching")
First let's take a step back. Finding the issue is not the same as finding the symptom. Symptoms can come from several sources. QA specialists, end users, other developers and testing frameworks can all relate a symptom of an issue. Sometimes it is a complete lack of functionality. Other times its a failing feature or not acheiving an expected result. The first step in finding the bug is not going hunting for it. First we must reproduce the issue.

Reproducing the issue will not only ensure that we are looking for the right bug, it will also give us clues as to where the bug is hiding. When talking to my manager about this he said: "Think about a problem that occurs on production but not in dev. What's different between the environments that might cause the issue? Does the bug only manifest itself on new builds, but not existing environments?" Once we can reproduce the bug, we are ready to find it. 

One of the initial paths to a solution can be found using our experience as developers. This is especially true when working in the same system for many years. Common patterns emerge and knowing the common causes (cache invalidation or stale cache, load balanced environments, etc) can save time and frustration.

But if the system is unknown, we need to build up that experience to be able to start to recognize those patterns. In Web Development, one of the first questions to answer is where in the "stack" is the bug. The "stack" are the tools used to produce a website or web application. For simplicity, and also to break down which tools we could use, the two major parts we are going to focus on regardless of technology are client side and server side. If the bug is client side most often the troubleshooting will take place in a browser using built-in or add-on development tools. Server side troubleshooting will often take place in the code base or possibly in the data source. Because the data source can be so variant, this article will focus on the code base.

Once we know where to start our search the next step is to break out the toolbox. Metaphorically a troubleshooting toolbox would contain inspectors, debuggers, profilers and explorers. An inspector allows a developer to use the built-in or third party tools to select an element and see the "source" associated. 

##Debugging 

Debuggers can be found in those same developer tools; in a browser to assist in troubleshooting JavaScript or can be added to a server to troubleshoot "back-end" code. Debuggers allow a developer to set a break-point, or place to suspend executing code. During this suspension variables can be examined and sometimes interacted with. These tools can also allow us to move through the execution of the code. Showing what code was executed up to that point and proceed with executing the code step by step. The right debugger depends on the code base used. To find one use the lessons learned in [Part 1](Part 1) and search for the language used and the keyword "debugging". 

##Profiling

Profilers measure the performance of the code. This is less about what is causing something to fail, although it can diagnose timeouts, and more about how long it takes to do things. So in performance troubleshooting profiling is the key skill to have. Daniel Sasser, a Phase 2 Developer, has a great article on profiling for [Profiling Drupal](http://www.phase2technology.com/blog/profiling-drupal-performance-with-phpstorm-and-xdebug/).

##Analyzing

Our last tool is probably one of the least assuming but helps analyze some of the most important pieces of troubleshooting data. An explorer (or analyzer or reader) is a tool for making it easier to traverse log data. Having a good explorer can turn hours of combing through txt files or rows in a database into a few minutes of targeted search and queries. Some of these tools are built into the OS, such as Console in OSX. Other can be found for the OS or code base that is being analyzed, such as http://goaccess.io/.

##Fixing the issue
![Fixing](/images/blog/fixing.jpg "Fixing")
So we found the issue. Now we need to fix it. Depending on experience this can be a simple or daunting task. There are times when 8-10 hours of troubleshooting will result in a few minutes of code updates. But if you don't know what to do next, there are a many resource at our disposal.

There is a 4 letter acronym that has existed since the time that programs were invented (that may be an exaggeration) that gently reminded developers that the person that designed the software they were working with usually provided documentation. This is still true now. Documentation can be spread through various different channels. If the issue is related to the language the application is written, most languages have extensive documentation on how the language should be used properly to resolve the issue. 

Other sources of a bug can be found in the implementation of an API or within custom code. Most API's also provide good documentation, though sometimes not in the language we might be working with. Well written custom code should provide documenation via comments about the methods and classes used. However, when we need help on how to implement an API, but the example is not in right language; or the comments in the custom code are unhelpful or incomplete (We've all done it.), there are other sources of documentation. Once we know the cause of the issue, searching online for a solution can provide help in both of these situations. See the previous part of this series for more information on how to search for those solutions.

##Postfix
Once our solution is in place we should return to where we started. Trying to reproduce the issue. This will confirm our solution as the right one. Now that we know what the solution is and it works, what is next. 

One concern is how to deploy the fix. Another would be to provide others with a way use that solution. Both of these can be resolved by creating a patch. A patch provides for incorrect code to be removed as well as new or updated code to be applied. This allows for the deployment of a fix to specific parts of the code, without having to update the entire code base. A patch can also be shared with others so they can also update their code. It can also be included in the release of the next version of distrubuted code. 

Another concern is regression. You have taken the time to troubleshoot and fix the issue; you pat yourself on the back and think that your journey is at its end. But it is not. Development usually involves several systems being linked together. With all of this interoperability changes in one system almost always affect another. The fix you made may have introduced a new bug or uncovered an existing issue that was obfuscated before the changes that were made. To mitigate this, always  

##Making better code help others troubleshoot
I don't think a blog post about troubleshooting would be complete without acknowledging ways to help others troubleshoot our code. Code smell, according to [Martin Fowler](http://martinfowler.com/bliki/CodeSmell.html), "...is a surface indication that usually corresponds to a deeper problem in the system".  This can be helpful during troubleshooting as it could lead to underlying issues. But it can also be a "red herring". The less "smelly" our code is, the better chance the next person has in troubleshooting. This can be done by refactoring our code, making it easier to follow how a system works.

But no matter how code "smells" the best way to help others troubleshoot your code is to provide comments. This is not only helpful to others, it will help you troubleshoot your own code; 12 months later, after 4 other projects and you have no idea why you wrote that function the way you did. But luckily you made good comments and are ready to add a new feature. A skill that will be covered in Developer Soft Skills Part 3: Enhancing/Customizing.
