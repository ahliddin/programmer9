---
layout: post
title: "Notes from Java Concurrency in Practice"
author: ahliddin
categories:
image: /assets/images/a-mind-for-numbers/java-concurrency-in-practice.png
featured: true
comments: true
tags: java,programming,concurrency
keywords:
    - java
    - programming
    - multithreading
    - parallel programming
    - science
    - learning
    - brian goetz
description: "Book notes from Java Concurrency in Practice"
---
I read the [Java Concurrency in Practice](https://www.amazon.com/gp/product/0321349601) by legendary Brian Goetz about four years ago
and collected a lot of notes in my physical notebook.
The purpose of this post is to refresh my memory by going through the notes and to publish them for everyone else's benefit.  
The book was written in 2006 - a very long time ago, but [according to Brian Goetz](https://stackoverflow.com/a/10214606/3082046) 
all of it is still relevant, missing only the coverage of some new features.  
However, the [Project Loom](https://wiki.openjdk.java.net/display/loom/Main) might be a rather strong reason for a new version of the book.  
Anyway, here are my notes from the book.

***
Threads are everywhere - era of multicore processors!  
Even if your app is single-threaded you might use a framework that calls your classes from multiple threads, so they need to be thread-safe.

***
*Object's state* is its data, stored in state variables such as instance or static fields.  
*Shared variable* is the one that can be accessed by multiple threads.

- Don't share the state variable across threads
- Make the state variable immutable
- Use synchronization whenever accessing state variable

***
A class is *thread-safe* when it continues to behave correctly when accessed from multiple threads.  
*Thread-safe* encapsulate any needed synchronization, so that clients need not provide their own. 

***
We collectively refer to **check-then-act** and **read-modify-write** sequences as *compound operations.  
*Compound operations* must execute atomically in order to remain *thread-safe*.  
Where practical, use existing thread-safe objects - *AtomicLong, AtomicReference<T>, ConcurrentHashMap*, etc.

