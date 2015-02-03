---
layout: post
title: Developer Soft Skills Part 1 - Online Research
cover:
date:   2014-11-23 21:00:00
categories: posts
---

#Developer Soft Skills

One of my earliest jobs I had was customer service for a call center. I worked for many clients that all had training specific to their service. No matter the type of training, whether technical or customer oriented, soft skills were always a included. [Margaret Rouse](http://searchcio.techtarget.com/definition/soft-skills) said, "Soft skills are personal attributes that enhance an individual's interactions, career prospects and job performance. Unlike hard skills, which tend to be specific to a certain type of task or activity, soft skills are broadly applicable." 

In this series I will be discussing what I call "developer soft skills". The hard skills in development are (among others) logic, languages and structure.  Developer soft skills are those that help a developer accomplish their tasks outside of that knowledge.  I will be covering the following topics:

* Online research
* Troubleshooting
* Enhancing/Customizing
* Integrating
* Architecting

#Part 1: Online Research

One of the first skills a developer should master is online researching. This is an area with some controversy (which will be discussed later) but a necessary skill for learning about new technologies, expanding your knowledge and solving problems.

One of the best reasons for research is continuous education. In the military, education and medical professions continuing education is required to keep up on updated information, concepts and procedures. As a developer continuing to grow our skill set helps us develop better projects by using better code, better tools and better methods.

###Search engine queries

When researching a topic on the internet it usually involves using a search engine. Understanding how a search engine works and how to get to the results.There are two parts to how a search engine works. Part one is data collection and indexing. Part two is searching or querying that index. I will be focusing on how to write the best possible query, to learn more about how search collect and index data see [this](http://www.google.com/insidesearch/howsearchworks/thestory/) link. In order to write good queries we should understand how search engines respond to what we type into the search box. Early search results were rendered based on simple (by today's standards) comparison of search terms to indexed page word usage and boolean logic. Since then search engines have started to use [natural language]( http://research.google.com/pubs/NaturalLanguageProcessing.html) queries.

So we can get better results by using this to our advantage. If I wanted to research how to make a calendar with the Java programming language. instead of searching for keywords and distinct ideas "java -script calendar" by them selves; use natural language to include phraseology and context in our queries: "how can I make a calendar with java". The first result from the keyword search returns a reference to the Java Calendar class. The first result from the second query return example code on writing a calendar in Java. The better the query the better the results.

###Search result inspection
Once we have the right query we can then turn our attention to the results. One of the first things I do limit the results to a date range. This prevents results from the previous decade or further to be displayed with more recent and applicable ones. Another way to focus our search is to limit the site that the search takes place on. If we know we want to search for a jQuery function search jquery.com.

![Date Search](/images/blog/date_search.png "Date Search")

Once we have filtered our results its time for further inspection. When viewing a results page, the first thing I will look for is the context of the article or post. Does the author and/or site have a lot of ads? This can sometimes mean that the site is more about making money then providing good answers. Does the page have links or other references to related topic or ideas? This can show if the author is knowledgeable in the subject matter.

###The controversy
Earlier I mentioned online researching can be a controversial topic. One of the points of controversy is discussed in Scott Hanselman's blog post, [Am I really a developer or just a good googler?](http://www.hanselman.com/blog/AmIReallyADeveloperOrJustAGoodGoogler.aspx). While I agree with his major point, that researching bad code can be dangerous, I contend that using a search engine can produce good results and learning opportunities.

The other controversy is found almost anytime you search for any programming topic. One site or group of sites is predominant in almost every result: Stack Overflow or the Stack Exchange group of sites.  Several articles have been written about reasons [not to use](http://sergworks.wordpress.com/2012/09/26/why-stackoverflow-sucks/), [consequence of using](http://meta.stackexchange.com/questions/171172/stack-overflow-technology-makes-me-write-bad-answers) and why [some developers no longer use](http://michael.richter.name/blogs/why-i-no-longer-contribute-to-stackoverflow) Stack Overflow.

Again, these arguments make some good points. And again I think that using Stack Overflow correctly, just like good use of search engines, can produce good results. One of my first reasons for using a Stack Exchange site is community. These sites have leveraged Stack Exchange Q&A methodology for their specific topic or technology and can be a great resource on how to solve a problem within the bounds of that community.  One of my development mentors told me that there were 1,000's of ways of solving a programming problem and usually several wrong ones. The key is to not do one of the wrong ones and try to find one of the best ones. Searching within a Stack exchange site for answers can highlight the wrong ones but also provide the ones that work best in that system.

Here is an example of a Stack Overflow Drupal community response that came up when I searched for:  "drupal create term programmatically".

![Stack Overflow](/images/blog/stack_overflow.png "Stack Overflow")

This response is correct, but if you look at the [link] (https://api.drupal.org/api/drupal/modules%21taxonomy%21taxonomy.module/function/taxonomy_save_term/6) provided, you will see this is for Drupal 6. If you were looking for how to do this in Drupal 7 for instance the answer provided would not be correct. We could have improved our results by adding "Drupal 7" to our query.  But most important is to keep in mind that sites like Stack Overflow, or other community sites such as PHP.net include a mix of user generated responses. Meaning anyone can respond without being vetted. 

###Keep going
The best piece of advice I can offer for the arguments against using online search results and Stack Overflow is: "This is not the end."  Keep going past the result and research the answer. Don't just copy and paste the code. Don't just believe the top rated answer or blog post. Click the references sited, search the function or api calls that are in the answer, make the research apart of your knowledge. And then give back by writing about your article or posting your own answers. Answering questions can sometimes be just as powerful a learning tool as searching for them.

In the next post I will discuss a good use case for Stack Exchange sites, Developer Soft Skills Part 2: Troubleshooting.
