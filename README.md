trunkclub.github.io
===================
Trunk Club Engineering blog, hosted on GitHub Pages.

# Getting started

1. Check out the tech blog [intro deck on slid.es](slid.es/jhabdas/trunkclub-techblog).
2. Use [Prose.io](http://prose.io) or GitHub to author content without cloning.

# Hacking on the framework

1. Clone the repo
2. Check ruby version with `ruby --version` and, if necessary, switch to ruby 1.9.3 (e.g. `rvm use 1.9.3`)
3. Install dependencies with `gem install bundler` followed by `bundle install`
4. Run `git checkout -b source origin/source` to access the blog source code

Check out the list of [3rd party plug-ins](https://github.com/imathis/octopress/wiki/3rd-party-plugins) for ideas.

# Deployments
To deploy changes to source, run `rake generate` followed by `rake deploy`. Octopress should take care of the rest.

# Tips for creating new posts

- See [Octopress blogging basics](http://octopress.org/docs/blogging/) to get aquainted with the rake tasks available or just pull up the `Rakefile` and start reading.
- We're using Redcarpet, so use github flavored markdown ([cheet sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet))
