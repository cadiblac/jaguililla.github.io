---
layout: post
title:  The Making Of
excerpt: >
  The idea of writing a blog came to my mind long time ago. I started two times, but finally the
  third is the good one. First because I found a good platform to write posts and create my own
  design and second because I already have a bunch of stories to write about...
categories: Projects
tags: Blog Jekyll
---

The concept
-----------

The idea of writing a blog came to my mind long time ago. I started two times, but finally the
third is the good one. First because I found a good platform to write posts and create my own
design and second because I already have a bunch of stories to write about.

This first post (the second really) is about the blog itself. Not only from the code point
of view, but also from the design and concept perspectives.

The name's origin is pretty clear. It is [René Descartes] [Cogito] with a geek twist ;) 
The point is that you cannot code without thinking, but... do we always think as hard as we
should? For the favicon, I will let the reader find out what it is!

At the beggining I wanted to focus on the "thinking" part and [Rodin]'s [Thinker] came to my 
mind. Later I changed my mind to focus on the "programming side", then I decided to use a
computer picture as the background. I considered "famous" computers as HAL 9000 and Eniac, 
in the end I used the latter one, focusing in the old times of computing.

The looks are "old style" or "vintage" as modern people like to call it nowadays. I wanted to
reflect the origins of this craft and that is why the colors are dark and greenish (like my
first monitor ;)

[Renee Descartes]: http://en.wikipedia.org/wiki/Ren%C3%A9_Descartes
[Cogito]: http://en.wikipedia.org/wiki/Cogito_ergo_sum
[Rodin]: http://en.wikipedia.org/wiki/Auguste_Rodin
[Thinker]: http://en.wikipedia.org/wiki/The_Thinker


The implementation
------------------

I saw some premade themes and sites done with Jekyll,

- jekyll new <user>.github.io
- atom.xml and _includes taken from 'UP'
- sitemap.txt and rss.xml taken from jekyllbootstrap.com
- templates from startbootstrap
- Why Jekyll instead Jekyll bootstrap? MVB (minimum viable blog)
- Install: ruby, gem, jekyll, python, pygments
- Selecting a theme (going with vanilla Jekyll + templates (startbootstrap) )
- Operation: using make (available from all Unix, in the end it has to be Unix... so who cares
  about multiplatform)
- Generating 'syntax' for pygments (pygmentize -S monokai -f html > css/monokai.css)
- Using CDNs instead copying libraries
- Deployment (git commands)
- References (themes, info, jekyll)
- Using webstrap
- crossdomain, humans & robots from HTML5 Bootstrap
- If page isn't updated, check Github repo settings (Github Pages section)


Conclusion
----------

way harder than using jekyllBootstrap, and other classical blog engines. In return
you get flexibility and learn things reusable (not custom templates for blogger and so on).
The process of doing it was fun


(Re)using it
------------

If you want to use the code for your own site, you can refer to the [readme.md] file and check
how to change it to suit your own needs.

[readme.md]: http://github.com/jamming/jamming.github.io/blob/master/readme.md
