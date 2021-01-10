---
layout: post
title: "Notes from Java Concurrency in Practice"
author: ahliddin
categories:
image: /assets/images/java-concurrency-in-practice/java-concurrency-in-practice.png
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
We collectively refer to **check-then-act** and **read-modify-write** sequences as *compound operations*.  
*Compound operations* must execute atomically in order to remain *thread-safe*.  
Where practical, use existing thread-safe objects - *AtomicLong, AtomicReference&#60;T&#62;, ConcurrentHashMap*, etc.

***
A *synchronized block* has two parts: reference to an object that will serve as the *lock*, and a block of code to be guarded by that.

{% highlight java %}
    synchronized (lock) {
        // modify shared state
    }
{% endhighlight  %} 

A *synchronized method* is a shorthand for a synchronization block that spans an entire method,
and whose *lock is the object on which the method is being invoked*.
{% highlight java %}
    synchronized void modifySharedState() {
        // modify shared state
    }   
{% endhighlight  %} 

These built-in locks (any java object) are called **intrinsic locks** or **monitor locks**.

***
*Intrinsic* locks are **reentrant** - if a thread tries to acquire a lock it already holds, it will succeed.

***
All accesses to a mutable state must be preformed with the same lock held - in this case, we say a variable is *guarded by that lock*.

***
Avoid holding locks during lengthy computations or operations at risk of not completing quickly (network, I/O operations, etc.)

***
Locking is not just about mutual exclusions; it is also about memory visibility.  
To ensure threads can see the most up-to-date values of shared mutable variables the reading and writing threads must synchronize on common lock.

***
**Volatile** keyword ensures that values updated are read/written to the main memory, not to local CPU caches.
[This is not from the book](http://tutorials.jenkov.com/java-concurrency/volatile.html)  
*Volatile* variables can guarantee only visibility; locking can guarantee both *visibility* and *atomicity*.  
*Volatile* is not good for compound operations. The most common use is completion, interruption or status flag.

***
**Thread confinement** - if data accessed only from single thread no synchronization needed.  
**Stack confinement** - an object can be accessed through local variables, which are intrinsically confined to executing thread.

***
Conceptually, you can think of ThreadLocal&lt;T&gt; as a Map&lt;Thread, T&gt; that stores thread-specific values.  
In reality, it's not implemented that way - values are stored in the Thread object itself (thread dies, data die).

***
An object is *immutable* if:
- Its state cannot be modified after construction
- All its fields are final
- it is properly constructed - "this ref" doesn't escape

Good practice to make fields final unless needed otherwise.

***
To *publish* an object safely: 
- Initialize an object ref from static initializer
- Store a ref into volatile variable or *AtomicReference* 
- Store a ref into a final field of a properly constructed object
- Store a ref into a field that is guarded by a lock


... to be continued







































