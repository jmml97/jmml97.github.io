---
title: The search for a static site generator
date: 2023-03-04
---

So I am once again having this urge to have a *technical* blog in my personal site. 

I just want to write about computer science related things I find out (at work or in my free time).

My old site was just an HTML file I had manually written with the information I needed. The website had nothing more.

But if I want to write a blog I need something more sohpisticated. I don't want to have to write all the HTML manually for every post.

But actually, how sophisticated does this tool need to be?

In the past I have used `jekyll`, which does not seem *cool* in 2023, and `hugo`, which has the potential to be way more complex than what I need.

Since what I needed now was just to parse a few Markdown files, convert them to HTML and obtain a list of said generated HTML files I thought that maybe a simple `bash` script that used `pandoc` was all that I needed.

But it is not that easy. I bumped into `barf`, which seemed to check all the boxed I needed. Except that it is not portable: it depends in the GNU versions of tools like `sed` and `date`, which are not the default ones in macOS.

I could have made it work there by installing said versions and modifying the script to work

I also wanted an RSS feed of the posts. 

I said well, I could implement my own.

Too much work.

I ended up using hugo, which I had used in the past.

Despite it seeming too complex for the task I wanted to achieve, I actually had a working version of the blog with the design I wanted in one morning.

Heavily inspired by the Berkeley Graphics website ().



