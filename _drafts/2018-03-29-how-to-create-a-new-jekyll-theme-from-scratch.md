---
layout: post
title:  "How to Create a new Jekyll Theme from scratch"
date:   2018-03-29 11:00:00 -0400
categories: web-development
---

## How to Create a new Jekyll Theme from scratch
	
	Build out the files base needed into a new theme directory</br>
	Open Terminal into your folder username.github.io</br>
	In Terminal type: <code>jekyll new-theme name-of-my-theme</code></br>
	Ref.: https://www.siteleaf.com/blog/making-your-first-jekyll-theme-part-2/ </br>
	</br>
	
	Edit the .gemspec
	The file is located in project-name/name-of-my-theme/name-of-my-theme.gemspec
    Modify the coresponding lines bellow
	<code>
	spec.summary       = %q{This is my custom Jekyll theme build for my personal website and testing purpose.}
    spec.homepage      = "https://github.com/sylvaindeschenes/sylvaindeschenes.github.io"
	</code>
	
	Install the gems that the theme depend on
	Edit the Gemfile
	The file is located in project-name/name-of-my-theme/Gemfile
	Add the lines bellow after the existing lines
	<code>
	gem 'github-pages', group: :jekyll_plugins
	</code>
	Open Terminal into your folder username.github.io/name-of-my-theme</br>
	In Terminal type: <code>bundle install</code></br>
	Ref.: https://github.com/github/pages-gem
	
	Add the theme to the website
	Edit the _config.yml
	Add this line: <code>theme: gingerbim-theme</code>
	
	
	Test the theme on the website
	Open Terminal into your folder username.github.io
	In Terminal type: <code>bundle exec jekyll serve --watch</code>
