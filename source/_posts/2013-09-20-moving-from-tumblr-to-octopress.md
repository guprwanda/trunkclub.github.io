---
layout: post
published: true
title: Moving from Tumblr to Octopress
comments: true
author: Josh Habdas
tags: 
  - octopress
  - jekyll
  - blogging
  - tumblr
  - prose.io
  - "travis-ci"
---

At Trunk Club, we love technology. It's at the core of our business and helps enable us to provide amazing user experiences both internally and externally. So, when asked recently to help provide opinion on our tech blog, I was excited for opportunity--until I saw the blog was hosted on Tumblr.

What's wrong with Tumblr? Nothing, really, except that, as an engineer who's been maintaining a technical blog for the last 5 years, I found it difficult to put words--let alone words with a opinion--on a platform I myself didn't embrace. So before writing these words, I felt compelled to move our tech blog away from Tumblr. Read on to learn about the Octopress migration, and how to set up a wicked quick, CMS-free blog with free hosting and then some.

<!-- more -->

Based on personal experiences with CMS-driven blogs like [WordPress and Drupal](http://www.habdas.org/drupal-7-for-wordpress-admins/), going CMS-free was the first requirement. This was primarily a performance play, as CMS-driven sites, even Wordpress with W3 Total Cache, CloudFront and any number of performance tweaks simply can't compete with a static site witout a jauggernaut of an app server behind it. There was no second requirement. It just had to be fast, and that's it.

At Trunk Club we write a lot of Ruby and CoffeeScript. So it seems fitting we should chose a blog which leverages one of those technologies. After looking briefly at Jekyll, I noticed Octopress. And after looking at Octopress, I noticed it could be hosted on GitHub pages--for free--and be build by Travis-CI (also for free). That's a whole lot of free, so let's briefly recap what we're getting high-level:

- Lightning fast, CMS-free blogging system based on the wonderful [Ruby language](https://www.ruby-lang.org/)
- Free hosting using GitHub with support for vanity URLs
- Free Continuous Integration using [Travis-CI](https://travis-ci.org/)

But why stop there? So I decided to take it a little further and:

- Open source the site to help the tech community see what's up at teh Trunk Club
- Add support for [Prose.io](http://prose.io/), to simplify the entire blogging process and open up post authoring to anyone--even without an environment
- Integrate the site with the 37signals' Campfire, so we'd be notified instantly about build status

Once the system design was complete, I [diagrammed it](http://www.gliffy.com/go/publish/4845414) so I could run it by some peers. The feedback I received was positive, so I started building. After a bit of trial and error, and reading, I ended up finding the following, excellent article which boils most of the setup process into a small number of easily reproducable steps:

http://rogerz.github.io/blog/2013/02/21/prose-io-github-travis-ci/

After running through the above instructions, I used the [Jekyll import tool](https://github.com/jekyll/jekyll-import) to pull the posts from our old tech blog on Tumblr, and given our relatively low tech blog engagement, opted to simply use `meta` redirects for old posts to prevent linkrot. Once that was done, I customized the URL structure for better canonical urls, and tailored the site's core config YAML and post frontmatter across the board.

After that, all that was left to go live was a simple DNS update and the addition of a `CNAME` file. And viola, I can write this post in markdown, edit it from my phone, the cost was nil, and the site is fast, open and everything but Tumblr. Let the blogging begin.