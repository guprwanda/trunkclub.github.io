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

What's wrong with Tumblr? Nothing, really, except that, as an engineer who's been maintaining a technical blog for the last 5 years, I found it difficult to voice an opinoin on a platform I myself didn't fully embrace. So before writing these words, I felt compelled to move our tech blog away from Tumblr. Read on to learn about the Octopress migration, and how to set up a wicked quick, CMS-free blog with free hosting and then some.

<!-- more -->

Based on personal experiences with CMS-driven blogs like [WordPress and Drupal](http://www.habdas.org/drupal-7-for-wordpress-admins/), going CMS-free was the first requirement. This was primarily a performance play, as CMS-driven sites, even Wordpress with W3 Total Cache, CloudFront and any number of performance tweaks simply can't compete with a static site witout a jauggernaut of an app server behind it. There was no second requirement. It just had to be fast, and that's it.

At Trunk Club we write a lot of Ruby and CoffeeScript. So it seems fitting we should chose a blog which leverages one of those technologies. After looking briefly at Jekyll, I noticed Octopress. And after looking at Octopress, I noticed it could be hosted on GitHub pages--for free--and be build by Travis-CI (also for free). That's a  lot of free, so let's briefly recap what we're building:

- Open source site to help illustrate how Trunk Club uses [Octopress](http://octopress.org/)
- Blog is of the CMS-free variety and based on the wonderful [Ruby language](https://www.ruby-lang.org/)
- Hosting righ tnow is free thanks to [GitHub Pages](http://pages.github.com/)
- Continuous Integration using [Travis-CI](https://travis-ci.org/)
- Support for [Prose.io](http://prose.io/), to simplify post authoring and enable blogging from a desktop or mobile web browser
- Integration with the 37signals' Campfire to post build notifications

After one of those back-of-the-napkin drawings I decided simply to [diagram the system](http://www.gliffy.com/go/publish/4845414) so I could run it by another engineer at TC. Feedback was positive, so I started building. After a bit of trial and error I ended up finding the following, excellent article, which boils most of the setup process into a small number of easily reproducable steps:

[Octopress+Prose+Github+Travis CI = Coders' Blog](http://rogerz.github.io/blog/2013/02/21/prose-io-github-travis-ci/)

After running through the above instructions, I used the [Jekyll import tool](https://github.com/jekyll/jekyll-import) to pull the posts from our old tech blog on Tumblr used simple `meta` redirects for old posts to prevent linkrot and allow us to move to a better canonicalized URL (somewhere an SEO guy cheers). Once that was done I modified the Octopress config YAML and post frontmatter, finished up with various copy editing and post migration clean-up tasks.

After that, all that was left to go live was a simple DNS update and the addition of a `CNAME` file. And viola, I can write this post in markdown, edit it from my phone, the cost was nil, and the site is fast, open and everything but Tumblr. Let the blogging begin.