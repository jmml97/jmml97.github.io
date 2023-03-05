---
title: Choosing a static site generator
date: 2023-03-05
---

At some point during the past week, I had an idea for a blog post.
Then I realized I did not have a blog.
My old site was just an HTML file I had manually written, as if we were living in the early 2000s.
The website had nothing more.

But if I wanted to write a blog I needed something more sohpisticated.
Manually coding the HTML for every post I wanted was out of the question.
As it was some kind of CMS like [Wordpress](https://wordpress.org/): that was too complicated.
I simply wanted to write about computer science-related topics I came across at work or in my free time and be able to host them as plain HTML files.

I had experimented with static site generators in the past, including [Jekyll](https://jekyllrb.com/) and [Hugo](https://gohugo.io/), but I found Jekyll outdated and Hugo more complex than necessary.
I believed that a simple Bash script that used [Pandoc](https://pandoc.org/) to parse a few Markdown files and generate HTML would suffice.

However, I soon discovered that it was not as easy as I thought.
I am not very fluent in Bash, so I did a search to look for some pre-made scripts.
The options I found included [Barf](https://barf.bt.ht/), which seemed to meet my needs, but then I learned that it was not portable since it relied on GNU versions of `sed` and `date`, which are not included by default on macOS.
Since I work on both Windows, using the [Windows Subsystem for Linux](https://learn.microsoft.com/en-us/windows/wsl/), and macOS, I needed a solution that would work on both platforms without requiring additional software or modifications.

Then I considered implementing my own generator in Go, a language I am familiar with, or in Rust, which would be a good opportunity to learn.
However, I quickly realized that this would be a time-consuming endeavor.
As [some](https://lobste.rs/s/rfsabk/what_are_you_doing_this_weekend#c_vbbii4) [people](https://lobste.rs/s/rfsabk/what_are_you_doing_this_weekend#c_igrhhw) pointed out to me, did I really want to spend a lot of time writing the generator instead of writing blog content?

Eventually, I decided to give Hugo another try, and was pleasantly surprised that it was not as complex as I remembered.
The `hugo new` commands were useful to create a site and theme boilerplate that I could modify easily.
In fact, I was able to create a working version of my blog, complete with the design I wanted (heavily inspired by the [Berkeley Graphics website](https://berkeleygraphics.com/)), in just one morning.

And that is how I ended up with the blog you are currently reading.
With the technical details sorted out (which, in the end, was the easy part), the hard part is yet to come: continuing to write more content.
See you soon!