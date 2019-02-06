---
layout: post
title:  "Largest Survey of Java Developers.. ever"
author: ahliddin
categories:
image: /assets/images/
featured: true
comments: true
tags: programming,
keywords:
    - programming
    - java survey
description: The results of the survey with 10,500 Java developer participants
---

Recently I read a great article by [Simon Maple](https://twitter.com/sjmaple) and [Andrew Binstock](https://twitter.com/platypusguy) -
_The Largest Survey Ever of Java Developers_ on [Java Magazine](http://www.javamagazine.mozaicreader.com).
There were 10,500 Java developers participating in the survey.

Here's an extract of what I found most interesting.

#### Which Java vendor’s JDK do you use in production for your main applications?
The obvious winners so far are Oracle JDK and OpenJDK. Although with upcoming changes in licencing and support the figures might quite change in a next survey.
I didn't quite understand how 1% of those Java developers survive programming in *Java* with *'None'* JDK. I didn't find any explanation in the original article as well.

{% include image.html
    caption="Which JDK developers use?"
    url="/assets/images/largest-java-survey-ever/popularity_of_JDKs_amongst_Java_developers.png"
%}

#### What Java EE version do you use for your main applications?
38% of Java developers don't use Java EE at all. Hello, [Spring Framework](https://spring.io) :-).
Probably there are some Swing and JavaFX developers among them too, though.

{% include image.html
    caption="Which Java EE developers use"
    url="/assets/images/largest-java-survey-ever/what-JavaEE-developers-use.png"
%}


#### What is the principal JVM language you use for your main applications?

Java is a badass dominant here.
Considering that for the past few years people have been talking about *Kotlin* a lot, only 2.42% of respondents use it as a primary language in their projects.
Although it beats *Scala*, I'm surprised to see it's behind *Clojure*.

{% include image.html
    caption="What JVM language developers use"
    url="/assets/images/largest-java-survey-ever/JVM_language_developers_use.png"
%}


#### Which IDE do you develop with?
IntelliJ IDEA is the best IDE I ever coded in. I used Eclipse and NetBeans before, but once I tried IntelliJ I never went back.
I have nothing against *vi/vim* editor, I love to use them for quick editing of files or writing *bash* scripts.
In fact, I think that any developer should have some basic knowledge of using *vim* and some *bash* scripting.
But using it as an IDE for Java project.. come on. If those 3% of respondents were actually serious about using *vi/vim* as a primary IDE,
then they probably commute to work on horses and treat appendicitis with blood-lettings and laxatives.

{% include image.html
    caption="Which IDE developers use"
    url="/assets/images/largest-java-survey-ever/which_IDE_developers_use.png"
%}