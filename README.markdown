trunkclub.github.io
===================
Trunk Club Engineering blog, hosted on GitHub Pages.

[![Build Status](https://travis-ci.org/trunkclub/trunkclub.github.io.png?branch=source)](https://travis-ci.org/trunkclub/trunkclub.github.io)

# Getting started

1. Check out the tech blog [intro deck on slid.es](http://slid.es/jhabdas/trunkclub-techblog).
2. Use [Prose.io](http://prose.io) or GitHub to author content online.
3. Follow the instructions below if you'd like to wrench on the app or deploy manually.

# Hacking on the framework

1. Clone the repo
2. Check ruby version with `ruby --version` and, if necessary, switch to ruby 1.9.3 (e.g. `rvm use 1.9.3`)
3. Install dependencies with `gem install bundler` followed by `bundle install`
4. Run `git checkout -b source origin/source` to access the blog source code
5. Add "[ci skip]" to commit message to prevent Travis-CI from triggering a build for any given commit

Check out the list of [3rd party plug-ins](https://github.com/imathis/octopress/wiki/3rd-party-plugins) for ideas.

# Deployments

- Occur automatically via [Travis-CI](https://travis-ci.org/trunkclub/trunkclub.github.io) anytime the source branch changes.
- Can be performed manually by runing `rake generate` followed by `rake deploy` from source after cloning, and once the `rake setup_github_pages` task has been run.

## Tips for creating new posts

- See [Octopress blogging basics](http://octopress.org/docs/blogging/) to get aquainted with the rake tasks available or just pull up the `Rakefile` and start reading.
- We're using Redcarpet, so use github flavored markdown ([cheet sheet](https://github.com/adam-p/markdown-here/wiki/Markdown-Cheatsheet))


## What is Octopress?

Octopress is [Jekyll](https://github.com/mojombo/jekyll) blogging at its finest.

1. **Octopress sports a clean responsive theme** written in semantic HTML5, focused on readability and friendliness toward mobile devices.
2. **Code blogging is easy and beautiful.** Embed code (with [Solarized](http://ethanschoonover.com/solarized) styling) in your posts from gists, jsFiddle or from your filesystem.
3. **Third party integration is simple** with built-in support for Pinboard, Delicious, GitHub Repositories, Disqus Comments and Google Analytics.
4. **It's easy to use.** A collection of rake tasks simplifies development and makes deploying a cinch.
5. **Ships with great plug-ins** some original and others from the Jekyll community &mdash; tested and improved.


## Documentation

Check out [Octopress.org](http://octopress.org/docs) for guides and documentation.


## Contributing

[![Build Status](https://travis-ci.org/imathis/octopress.png?branch=master)](https://travis-ci.org/imathis/octopress)

We love to see people contributing to Octopress, whether it's a bug report, feature suggestion or a pull request. At the moment, we try to keep the core slick and lean, focusing on basic blogging needs, so some of your suggestions might not find their way into Octopress. For those ideas, we started a [list of 3rd party plug-ins](https://github.com/imathis/octopress/wiki/3rd-party-plugins), where you can link your own Octopress plug-in repositories. For the future, we're thinking about ways to easier add them them into our main releases.


## License
(The MIT License)

Copyright © 2009-2013 Brandon Mathis

Permission is hereby granted, free of charge, to any person obtaining a copy of this software and associated documentation files (the ‘Software’), to deal in the Software without restriction, including without limitation the rights to use, copy, modify, merge, publish, distribute, sublicense, and/or sell copies of the Software, and to permit persons to whom the Software is furnished to do so, subject to the following conditions:

The above copyright notice and this permission notice shall be included in all copies or substantial portions of the Software.

THE SOFTWARE IS PROVIDED ‘AS IS’, WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.


#### If you want to be awesome.
- Proudly display the 'Powered by Octopress' credit in the footer.
- Add your site to the Wiki so we can watch the community grow.
