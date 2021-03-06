---
layout: post
title: "Largest Java Developer Survey 2018"
author: ahliddin
categories:
image: /assets/images/largest-java-survey-ever/java-developer-survey.png
featured: true
comments: true
tags: programming
keywords:
    - programming
    - java
    - survey
    - java survey
    - java survey 2018
    - jdk
    - java infographic
    - developer survey
    - developer infographic
description: The results of the survey with 10,500 Java developer participants
---

Recently I read a great article by [Simon Maple](https://twitter.com/sjmaple) and [Andrew Binstock](https://twitter.com/platypusguy) -
_The Largest Survey Ever of Java Developers_ on [Java Magazine](http://www.javamagazine.mozaicreader.com).
There were 10,500 Java developers participating in the survey.

Here's an extract of what I found most interesting.

#### Which Java vendor’s JDK developers mainly use?
The obvious winners so far are Oracle JDK and OpenJDK. Although with upcoming changes in licencing and support the figures might quite change in a next survey.
I didn't quite understand how 1% of those Java developers survive programming in *Java* with *'None'* JDK. I didn't find any explanation in the original article as well.


{% include image.html
    caption="Which JDK developers use?"
    url="/assets/images/largest-java-survey-ever/popularity_of_JDKs_amongst_Java_developers.png"
%}

#### What Java EE version Java developers mainly use?
38% of Java developers don't use Java EE at all. Hello, [Spring Framework](https://spring.io) :-).
Probably there are some Swing and JavaFX developers among them too, though.

{% include image.html
    caption="Which Java EE developers use"
    url="/assets/images/largest-java-survey-ever/what-JavaEE-developers-use.png"
%}


#### What JVM language Java developers mainly use?

Java is a badass dominant here.
Considering that for the past few years people have been talking about *Kotlin* a lot, only 2.42% of respondents use it as a primary language in their projects.
Although it beats *Scala*, I'm surprised to see it is behind *Clojure*.

{% include image.html
    caption="What JVM language developers use"
    url="/assets/images/largest-java-survey-ever/JVM_language_developers_use.png"
%}


#### Which IDE Java developers use?

IntelliJ IDEA is the best IDE I ever coded in. I used Eclipse and NetBeans before, but once I tried IntelliJ I never went back.
I have nothing against *vi/vim* editor, I love to use them for quick editing of files or writing *bash* scripts.
In fact, I think that any developer should have some basic knowledge of using *vim* and *bash* scripting.
But using it as an IDE for Java project.. come on. If those 3% of respondents were actually serious about using *vi/vim* as a primary IDE,
then they probably commute to work on horses and treat appendicitis with blood-lettings and laxatives.

{% include image.html
    caption="Which IDE developers use"
    url="/assets/images/largest-java-survey-ever/which_IDE_developers_use.png"
%}


#### Which build tool Java developers mainly use?

Some developers use different build tools in their projects,
so it's worth to note that the question in the survey was asking for the *principal build tool*
the developers use. The vast majority of projects are built using *maven*.

{% include image.html
    caption="Which build tool developers use"
    url="/assets/images/largest-java-survey-ever/which_build_tool_developers_use.png"
%}

#### Which CI tool Java developers use?
As most developers would expect, Jenkins wins the CI server race with a whopping 57% market
share. Its closest competitor is “None” at 21% of the vote, which almost matches the rest of
the competition combined (at 22%).

{% include image.html
    caption="Which CI tool developers use"
    url="/assets/images/largest-java-survey-ever/which_ci_tool_developers_use.png"
%}

#### Which source code management tool dev teams mainly use?
I'm *not* surprised to see Git dominating the graph below. I *am* surprised to see that *Subversion* (a.k.a SVN)
is still being used by 16% of the developers.

{% include image.html
    caption="Which source code management tool developers use"
    url="/assets/images/largest-java-survey-ever/which_vcs_developers_use.png"
%}


#### Which testing technologies Java developers use?
*Robert C. Martin* said in his [talk](https://youtu.be/p0O1VVqRSK0?t=679) about Professionalism in Software Development that
*"we [programmers] are the surgeons doing an open-heart surgery on the systems of companies.. we are the reason the company makes money or loses money..
we are the ones who hold within our hands the lifeblood of the company"*.

And yet 10% of developers answered that they use *None* of testing technologies.. *none*..
Well hello, sleepless night!

I honestly hope that those 10% of participants are just self-learning developers or students that aren't working anywhere yet.

{% include image.html
    caption="Which testing technologies developers use"
    url="/assets/images/largest-java-survey-ever/which_testing_tech_developers_use.png"
%}


#### Which non-JVM languages Java developers use in their applications?
There are a lot of Java applications being written nowadays with JavaScript running in front end of it.
It's not clear from the survey if they meant pure JavaScript or any of its *syntactical supersets* like *TypeScript* as well.

I also wonder if those 8% of respondents that don't use any other non-JVM language in there project forgot to mention *SQL/JavaScript* as their DB query language.

{% include image.html
    caption="Which non-JVM languages used in project"
    url="/assets/images/largest-java-survey-ever/which_non-JVM_languages_developers_use.png"
%}


#### Which web frameworks Java developers?
I only worked with Spring MVC and Spring Boot and I'm glad to see that they are on the top of the list.
It's interesting though that Spring Boot has overtaken the Spring MVC.

{% include image.html
    caption="Which web frameworks developers use"
    url="/assets/images/largest-java-survey-ever/which_web_frameworks_developers_use.png"
%}


#### Which ORM frameworks developers use?
Note in the original article: *Developers could choose more than one answer, so totals do not equal 100%.*

More than half of the developers use *Hibernate*, surprise!

As for 23% that answered *plain old JDBC* and 20% that answered *None* the numbers might not be reflecting reality.
Since JDBC is not ORM framework those who said *None* might still be using the plain old JDBC.

{% include image.html
    caption="Which ORM frameworks developers use"
    url="/assets/images/largest-java-survey-ever/which_ORM_developers_use.png"
%}

#### Which database Java developers use?
Oracle is on the top of the list, then comes MySQL and PostgreSQL.
Only 9% of Java developers use *Microsoft SQL*, which is not surprising because it's the *C#*'s niche.

MongoDB is the highest *NoSQL* database with 5%, higher than IBM's relational database DB2.

{% include image.html
    caption="Which database developers use"
    url="/assets/images/largest-java-survey-ever/which_database_developers_use.png"
%}

#### Which application server developers mainly use?
Not much to add here, *Tomcat* rules.

{% include image.html
    caption="Which application server developers use"
    url="/assets/images/largest-java-survey-ever/which_application_server_developers_use.png"
%}

#### How often Java developers release new versions of code?
7% of developers release multiple times a day.. that's a bit more than I anticipated.
Usually it's the big players that hire geniuses and have streamlined processes can afford that..

{% include image.html
    caption="How often do developers release new version"
    url="/assets/images/largest-java-survey-ever/how_often_release_code.png"
%}

#### Where Java developers located?
The majority of developers are located in Europe and yet it's hard as never before to hire a good software developer.. at least in Prague.

{% include image.html
    caption="Where developers located"
    url="/assets/images/largest-java-survey-ever/where_developers_located.png"
%}

#### Age distribution of Java developers?
The majority of the software developers (38%) are 30 - 40 years old.

{% include image.html
    caption="Age distribution of Java developers"
    url="/assets/images/largest-java-survey-ever/developer_age.png"
%}

#### Where developers get information about Java online?
The actual winner here should be Google.
It's just happens that most of the answers are found in Stack Overflow..

{% include image.html
    caption="Where developers get information"
    url="/assets/images/largest-java-survey-ever/where_developers_get_info.png"
%}

#### How many of Java developers are members of a JUG?
Here's what developers replied to the question "Are you a member of JUG?".
Only 7% are the active members of JUGs.
13% of those who visit 1-2 times per *year* aren't far from another 13% who don't attend meetings at all.

{% include image.html
    caption="How many developers are members of JUG"
    url="/assets/images/largest-java-survey-ever/are_you_JUG_member.png"
%}

#### How much do Java developers contribute to open source?
I wish I was not the majority here..
Open source is a great platform for combining the learning and contributing. BTW, here's the great article about [learning a new programming language by contributing to open source](https://hackernoon.com/unconventional-way-of-learning-a-new-programming-language-e4d1f600342c).

Most of the developers have some sort of a pet project that they work on in their free time, and finding extra time to
contribute to open source is not always easy, considering that 38% of developers are 30 - 40 years old, the time when people usually start getting married and having kids.. bye-bye free time.

{% include image.html
    caption="How much developers contribute to the open source"
    url="/assets/images/largest-java-survey-ever/developers_contribute_to_opensource.png"
%}