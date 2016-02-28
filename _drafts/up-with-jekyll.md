---
title: From 0 - 60 with Jekyll
author: joesepi
layout: post
description: Learning to Jekyll with only broken guitars
permalink:
categories:
  - Learning
tags: [ jekyll, static site ]
---


-----
> 1 | Jekyll

So what is Jekyll, exactly?Permalink


Jekyll is a simple, blog-aware, static site generator. It takes a template directory containing raw text files in various formats, runs it through a converter (like Markdown) and our Liquid renderer, and spits out a complete, ready-to-publish static website suitable for serving with your favorite web server. Jekyll also happens to be the engine behind GitHub Pages, which means you can use Jekyll to host your project’s page, blog, or website from GitHub’s servers for free.

Jekyll has a config file (next section) that tells it how to process basic text files. By default, it reads each page's meta data (simply placed at the top of each file. more below) and knows how to process it to generate a site of static html files. That meta data will say which layout it should use (page style layout or post style layout as two examples) and each layout will probably reference include files (more below but examples being: header, nav, footer). Blog posts are named a specific way, which depends on how you specify them in the config file, but an example being: _post/2016-0229-how-to-go-jekyll-with-only-broken-guitars.md.

1) https://jekyllrb.com/docs/home/


-----
> 2 | Directory structure 

Jekyll is, at its core, a text transformation engine. The concept behind the system is this: you give it text written in your favorite markup language, be that Markdown, Textile, or just plain HTML, and it churns that through a layout or a series of layout files. Throughout that process you can tweak how you want the site URLs to look, what data gets displayed in the layout, and more. This is all done through editing text files; the static web site is the final product.


READ THIS:
docs: https://jekyllrb.com/docs/structure/


-----
> 2 | Configuration

Jekyll has powerful and flexible configuration options that should be specified in a _config.yml file placed in your site’s root directory.

Good example from my site:
code: https://github.com/joesepi/joesepi.github.io/blob/master/_config.yml

As you get near the bottom, it gets less important at this stage of learning.


-----
> 3 | Front Matter

Front matter is where Jekyll starts to get really cool. Any file that contains a YAML front matter block will be processed by Jekyll as a special file. The front matter must be the first thing in the file and must take the form of valid YAML set between triple-dashed lines. Here is a basic example:

example:
---
layout: post
title: Blogging Like a Hacker
---

Between these triple-dashed lines, you can set predefined variables (see below for a reference) or even create custom ones of your own. These variables will then be available to you to access using Liquid tags both further down in the file and also in any layouts or includes that the page or post in question relies on.

docs: https://jekyllrb.com/docs/frontmatter/

Good example is a blog post from my site:
code: https://raw.githubusercontent.com/joesepi/joesepi.github.io/master/_posts/2015-12-17-lbb-show.md
page: http://joesepi.com/2015/12/17/lbb-show/


