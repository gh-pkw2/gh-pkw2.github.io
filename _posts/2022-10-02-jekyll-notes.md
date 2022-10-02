---
title: Jekyll Notes
date: 2022-10-02 15:00 -400
categories: [homelab, software]
tags: [jekyll, markdown]
---
# Jekyll - Static Web Site Generator

## Installation

To use Jekyll in Linux, you need to first install the Ruby development environment:
~~~bash
sudo apt update
sudo apt install ruby-full build-essential zlib1g-dev git
~~~

To install the RubyGems packages in a user's folder (instead of as root):
~~~bash
echo '# Install Ruby Gems to ~/gems' >> ~/.bashrc
echo 'export GEM_HOME="$HOME/gems"' >> ~/.bashrc
echo 'export PATH="$HOME/gems/bin:$PATH"' >> ~/.bashrc
source ~/.bashrc
~~~

Then install the Jekyll bundler:
~~~bash
gem install jekyll bundler
~~~

This documentation site is based on the Chirpy theme and the Chirpy quick start at [https://github.com/cotes2020/jekyll-theme-chirpy#quick-start](https://github.com/cotes2020/jekyll-theme-chirpy#quick-start)

## Creating a Post

Jekyll uses a [naming convention for pages and posts](https://jekyllrb.com/docs/posts/).

Create a file in the _posts folder with the format:
YEAR-MONTH-DAY-title.md

For example:
2022-10-01-hello-homelab.md
2022-10-02-jekyll-notes.md



## Resources
Some helpful links for Jekyll and Markdown:

- [Jekyll Website](https://jekyllrb.com/)
- [Markdown Cheat Sheet](https://www.markdownguide.org/cheat-sheet/)
- [Chirpy Theme Posts](https://chirpy.cotes.page/posts/write-a-new-post/)
- [Techno Tim's Documentation Site repo](https://github.com/techno-tim/techno-tim.github.io/tree/master/_posts)
