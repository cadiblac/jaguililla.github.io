---
layout: post
title:  The Making Of
categories: Projects
tags: Blog Jekyll
---

My blog rationale
- I think therefore I code
- Colors
- Rodin
- HAL 9000
- Vintage computers
- Contents

My blog (behind the scenes)

- jekyll new <user>.github.io
- atom.xml and _includes taken from 'UP'
- sitemap.txt and rss.xml taken from jekyllbootstrap.com
- templates from startbootstrap
- Why Jekyll instead Jekyll bootstrap? MVB (minimum viable blog)
- Install: ruby, gem, jekyll, python, pygments
- Selecting a theme (going with vanilla Jekyll + templates (startbootstrap) )
- Operation: using make (available from all Unix, in the end it has to be Unix... so who cares about multiplatform)
- Generating 'syntax' for pygments (pygmentize -S monokai -f html > css/monokai.css)
- Using CDNs instead copying libraries
- Deployment (git commands)
- References (themes, info, jekyll)
- Using webstrap
- crossdomain, humans & robots from HTML5 Bootstrap

Conclusion: way harder than using jekyllBootstrap, and other classical blog engines. In return
you get flexibility and learn things reusable (not custom templates for blogger and so on).
The process of doing it was fun

To use the code for your own site refer to the readme

{% highlight ruby %}
def show
  @widget = Widget(params[:id])
  respond_to do |format|
    format.html # show.html.erb
    format.json { render json: @widget }
  end
end
{% endhighlight %}
