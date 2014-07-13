---
layout: post
title:  The Making Of
excerpt: >
  The idea of writing a blog came to my mind long time ago. I started two times, but finally
  the third is the good one. First because I found a good platform to write posts and create my
  own design and second because I already have a bunch of stories to write about...
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

I saw some premade themes and sites done with [Jekyll], but finally I started from scratch to
have the minimal code I needed for my blog and to customize it freely from the start.

In order to blog with [Jekyll], you have to install the following software in your system:
- Ruby
- Gem
- Jekyll (obvious)
- Python
- Pygments (for syntax highlighting)
    
Then, to create the site structure, you have to execute the command
`jekyll new <user>.github.io`. This will generate the minimum files required by Jekyll to build
a site. The name doesn't need to follow that naming pattern if you are going to host the site
in other place.

For the design I chose Twitter Bootstrap. I found very good templates in [Start Bootstrap].
Like these two which I used for some parts of the design:

* [Modern Business][http://startbootstrap.com/modern-business]
* [Grayscale][http://startbootstrap.com/grayscale]

To generate the base (static) of the site I used html5 boilerplate (in a tool of my own called
Webstrap).

Using webstrap html5 boilerplate

crossdomain, humans & robots from HTML5 Bootstrap
  
I picked some files from other Jekyll blogs:

* The `atom.xml` and `_includes` files were taken from the [UP][up] theme. Note that UP's
  includes were modified for the blog.

* `sitemap.txt` and `rss.xml` were copied from [JekyllBootstrap].

Using CDNs instead copying libraries

Operation: using make (available from all Unix, in the end it has to be Unix... so who cares
about multiplatform)
  
Generating 'syntax' for pygments `pygmentize -S monokai -f html > css/monokai.css`

Deployment (git commands)

References (themes, info, jekyll)

If page isn't updated, check Github repo settings (Github Pages section)

[up]: http://github.com/caarlos0/up
[JekyllBootstrap]: http://jekyllbootstrap.com
[Start Bootstrap]: http://startbootstrap.com


Conclusion
----------

Starting a blog with [Jekyll] from scratch is way harder than using [JekyllBootstrap] or other 
blog engine. In exchange: you get flexibility, take advantage of your current knowledge (Git, 
HTML...) and you don't have to learn custom templates for closed products.

Also you will learn valuable things (about Web design and development) and have fun in the 
process!

As a side effect, I realized that static site generation can be useful for other purposes (not
only for blogs). For example, it can be used to generate software project's technical 
documentation.

Regarding this last point, I found a [Jekyll] wannabe in Java called [JBake] that looks very 
promising.

[Jekyll]: http://jekyllrb.com
[JBake]: http://jbake.org

(Re)using it
------------

If you want to use the code for your own site, you can refer to the [readme.md] file and check
how to change it to suit your own needs.

[readme.md]: http://github.com/jamming/jamming.github.io/blob/master/readme.md
