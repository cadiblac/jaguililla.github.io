---
layout: post
title:  David vs Goliath
categories: Tools Projects
tags: OOS Java Web Framework Microservices Performance Comparison
---

Yeah, it's been a looong time, but I'm back on track with the blog.

Today, I want to prove that being big is not always an advantage, and I want to do it comparing two
Web frameworks.

On one side, with green shorts, a lot of features... and even more annotations is: [Spriiiiing
Booot][Boot], on the other side with black pants, a funny name and a very simple approach is: 
[Saaaabina][Sabina]

Ladies and gentlemen, let the fight begin.

For this match, I did some tests to measure size, cpu usage, memory, etc. do not expect nothing
too fancy here anyway. If you are courious about the tests, you can check the code in this [Github
repository][Repository].

The project to test both frameworks was the simplest one (yes, a Hello World project). And the
tools I used to measure the performance were Bash shell scripts, [JMeter] and Java's [VisualVM].

System Information
==================

First of all I will describe the laptop used to run the tests:

    Architecture:          x86_64
    CPU(s):                8
    Thread(s) per core:    2
    Core(s) per socket:    4
    Socket(s):             1
    Model name:            Intel(R) Core(TM) i7-4712MQ CPU @ 2.30GHz
    CPU MHz:               1434.445
    CPU max MHz:           3300.0000
    CPU min MHz:           800.0000
    BogoMIPS:              4589.46
    L1d cache:             32K
    L1i cache:             32K
    L2 cache:              256K
    L3 cache:              6144K

                 total       used       free     shared    buffers     cached
    Mem:          7.7G       3.6G       4.1G       188M        36M       2.1G
    -/+ buffers/cache:       1.5G       6.2G
    Swap:         953M        27M       926M
    Total:        8.7G       3.7G       5.0G

Code Size
=========

The first comparison I made was about the code size. Here are the results:

## Spring Boot

    28  39 hello-boot/build.gradle
    18  34 hello-boot/src/main/java/hello/Hello.java
    46  73 total

## Sabina

    13  19 hello-sabina/build.gradle
    10  24 hello-sabina/src/main/java/hello/Hello.java
    23  43 total
    
The first column is the number of lines, and the second one the number of words. And as we can see
Sabina is nearly half the size of the Boot project.

Build Process
=============

Let's continue with the build time and binary bundle size. For this test I built both projects 
three times and then I picked the best results out of the three executions. These were the results:

## Spring Boot

    Command being timed: "/opt/gradle-2.4/bin/gradle -q --no-daemon -p hello-boot clean build"
    User time (seconds): 17.16
    System time (seconds): 0.39
    Percent of CPU this job got: 333%
    
    -rw-r--r-- 1 jam jam 11M Jul  9 00:53 hello-boot.zip

## Sabina

    Command being timed: "/opt/gradle-2.4/bin/gradle -q --no-daemon -p hello-sabina clean build"
    User time (seconds): 14.06
    System time (seconds): 0.26
    Percent of CPU this job got: 315%

    -rw-r--r-- 1 jam jam 4.2M Jul  9 00:52 hello-sabina.zip
    
There is no big difference in the compile times, but the size of the Sabina's binary bundle is less 
than half than the Boot one.

Runtime
=======

Finally, I executed 10,000 requests from 8 threads, to check the memory and CPU usage along 
with the requests per second per framework.

Results are screenshots of [JMeter] and [VisualVM], however, if you want to see the exact numbers,
you can clone the [repository][Repository] and run the test yourself.

Here are the results of my run:

## Spring Boot

![JMeter summary](https://raw.githubusercontent.com/jamming/boot-vs-sabina/master/results/summary-report-boot.png)
![VisualVM graphs](https://raw.githubusercontent.com/jamming/boot-vs-sabina/master/results/performance-boot.png)

## Sabina

![JMeter summary](https://raw.githubusercontent.com/jamming/boot-vs-sabina/master/results/summary-report-sabina.png)
![VisualVM graphs](https://raw.githubusercontent.com/jamming/boot-vs-sabina/master/results/performance-sabina.png)

As you can see Sabina's times are better, but the biggest difference is in the resources' usage. My
opinion on this is that all features Spring Boot has, impact its runtime performance.
 
So if you really need something fast and are not going to use all its features, is better if you
evaluate other options.

Disclaimer
==========

Of course, these two frameworks doesn't compete in the same league... and their feature set is
(to say it softly) not of the same size.

However, it was fun to compare both (though it was not a very rigorous benchmark) and the numbers
could be more precise.

I will repeat these tests with a more complete project. Ie: the [blog used in MongoDB 
courses][Blog].

Until them, you can check real framework benchmark's [here][Techempower]. These two frameworks are 
there, but Sabina didn't implement all tests (another TODO in my task tracker) and I am not sure
that Spring's version is the latest one.


[Boot]: http://projects.spring.io/spring-boot/
[Sabina]: http://there4.co/sabina/
[Repository]: https://github.com/jamming/boot-vs-sabina
[JMeter]: http://jmeter.apache.org/
[VisualVM]: https://visualvm.java.net/
[Blog]: https://github.com/jamming/sabina/tree/master/blog
[Techempower]: https://www.techempower.com/benchmarks/
