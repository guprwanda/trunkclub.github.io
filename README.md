trunkclub.github.io
===================
Trunk Club Engineering blog, hosted on GitHub Pages.

[![Build Status](https://travis-ci.org/trunkclub/trunkclub.github.io.png?branch=source)](https://travis-ci.org/trunkclub/trunkclub.github.io)

# Getting started

1. Check out the tech blog [intro deck on slid.es](slid.es/jhabdas/trunkclub-techblog).
2. Use [Prose.io](http://prose.io) or GitHub to author content online.
3. Follow the instructions below if you'd like to wrench on the app or deploy manually.

# Hacking on the framework

1. Clone the repo
2. Check ruby version with `ruby --version` and, if necessary, switch to ruby 1.9.3 (e.g. `rvm use 1.9.3`)
3. Install dependencies with `gem install bundler` followed by `bundle install`
4. Run `git checkout -b source origin/source` to access the blog source code

Check out the list of [3rd party plug-ins](https://github.com/imathis/octopress/wiki/3rd-party-plugins) for ideas.

## Deployments

- Occur automatically via Travis-CI anytime the `source` branch changes.
- Can be performed manually by runing `rake generate` followed by `rake deploy` from `source` after cloning, and once the `rake setup_github_pages` task has been run.

# Tips for creating new posts

- See [Octopress blogging basics](http://octopress.org/docs/blogging/) to get aquainted with the rake tasks available or just pull up the `Rakefile` and start reading.
- We're using Redcarpet, so use github flavored markdown ([cheet sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet))
