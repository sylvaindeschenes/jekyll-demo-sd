---
layout: post
title:  "How to build a Static Website using Jekyll on GitHub-Pages"
date:   2018-03-29 10:00:00 -0400
categories: Web-Development
---
## Here are the steps I have used to release this website

Disclaimer: I'm not a coder, I have acquired basic IT and coding knowledge by being exposed to developers and geeks. This tutorial is my personal documentation for the creation of this website. If I can do it, you ca most probably do it too.  

The options I have chosen during the creation of this website have been based on the following:
  
 - Strong Open-Source Distributions: The tools and softwares have to be open-source and well suported by their development community
 - Without Plugin: The Jekyll website has to keep its ability to be built by GitHub Pages (No disalowed plugin)
 - Free: The 3rd party services have to be free (at least for personal usage)
 - Simplicity: The simpliest way that follow the best standards and conventions  
 
 For the records, my computer setup was the following:

- Mac OSX High Siera 10.13.3 on a MacBook Pro (Retina, 15-inch, Mid 2015) and a Mac mini (Late 2014)
- Jekyll 3.7.3 was the default version at the moment of writting this article


1. [Setup GitHub-Pages](#setup-github-pages)
2. [Setup the Local environment](#setup-the-local-environment)
3. [Create a new Jekyll site](#create-a-new-jekyll-site)
4. [Publish the changes live on GitHub-Pages](#publish-the-changes-live-on-github-pages)
5. [Keep local environment synced with GitHub-Pages Gem](#keep-local-environment-synced-with-github-pages-gem)
6. [Add pertinent supported GitHub-Pages plugins](#add-pertinent-supported-github-pages-plugins)

7. [Setup to customise Minima theme](#setup-to-customise-minima-theme)
8. [Add Bootstrap 4 using BootstrapCDN and local SASS](#add-bootstrap-4-using-bootstrapcdn-and-local-sass) ***To be completed***
9. [Add Favicons](#add-favicons)
10. [Add Dynamic Copyright in the footer](#add-dynamic-copyright-in-the-footer)
11. [Add Categories filter](#add-categories-filter)
12. [Make blog post URLs SEO Friendly](#make-blog-post-urls-seo-friendly)
13. [Add Contact or any other Forms](#add-contact-or-any-other-forms)  
14. [Add Comments on blog articles using Disqus](#add-comments-on-blog-articles-using-disqus)
15. [Setup Google Analytics](#setup-google-analytics)    

16. [Setup a Custom Domain name](#setup-a-custom-domain-name)
17. [Speed Optomisation](#speed-optomisation)  
 
18. [Some Helful Tips](#some-helful-tips)  

### Setup GitHub-Pages

#### Create a GitHub account  
Ref.: [https://github.com/join][https://github.com/join]

#### Create a repo on GitHub for GitHub-Pages  
Login to your GitHub account and create a new repo following this naming convention: `username.github.io`  
Ref.: [https://pages.github.com](https://pages.github.com]https://pages.github.com)  

#### Add a README.md file to your site
Go to the GitHub project page of the repo
Scroll down to the bottom of the page and Press the green button "Add a README"  
Write `Hello` in it.  
Scroll down to the bottom of this page and press the green button "Commit new file"

#### Test you static website  
Open a browser and type [https://username.github.io](https://username.github.io)  
Expected: `Hello` is displayed on a blank page  

### Setup the Local environment

#### Install Brew  
In terminal type 
~~~
/usr/bin/ruby -e "$(curl -fsSL https://raw.githubusercontent.com/Homebrew/install/master/install)"
~~~  
Ref.: [https://brew.sh](https://brew.sh)  

#### Install Ruby  
In terminal type  
`brew install ruby`  
Ref.: [https://www.ruby-lang.org/en/documentation/installation/#homebrew](https://www.ruby-lang.org/en/documentation/installation/#homebrew)   

#### Install RubyGems  
In Terminal type  
`sudo gem update --system`   
Ref.: [https://rubygems.org/pages/download](https://rubygems.org/pages/download)    

#### Install Jekyll and Bundler gems  
In Terminal type 
`sudo gem install jekyll bundler`  
Ref.: [https://jekyllrb.com/docs/quickstart/](https://jekyllrb.com/docs/quickstart/)

### Create a new Jekyll site  
Open Terminal into your folder username.github.io  
(In my case: `/Users/sylvain/Sites/sylvaindeschenes.github.io`)  
Type `jekyll new .`  
*For a site without theme, type instead `jekyll new --blank .`
*If the folder is not empty you can force the override with `jekyll new . --force`

#### For an existing Jekyll site (Cloned Repository on another Computer)
Open Terminal into your folder username.github.io  
*In my case: `/Users/sylvain/Sites/sylvaindeschenes.github.io`  
Run `bundle install`
  
#### Build the website  
In Terminal type `jekyll serve` or `bundle exec jekyll serve`

#### Test the newly created Jekyll website locally  
Open a browser and type [http://127.0.0.1:4000](http://127.0.0.1:4000)   

#### Stop Jekyll local serever  
In Terminal press: `CTRL + C`  
 
### Publish the changes live on GitHub-Pages

#### Install GitHub Desktop for OSX  
Ref.: [https://desktop.github.com](https://desktop.github.com) 

#### Clone GitHub Repository to the Computer
Open Github Desktop  
Go to menu File/Clone Repository
Select the repository `username.github.io`
Select a destination on the computer like: `/Users/user/Sites/` and press "Clone"

#### Create a local branch
Go to menu Branch/New Branch and name the branch `local_myname` 
Create a commit on the `local branch` using the interface on the left-bottom corner. Name the Commit and press "Commit to local_myname"
  
#### Create and send a Pull Request  
Go to menu Branch/Create a Pull Request
The browser will open automatically or to your GitHub project page in a browser  
Merge the Pulls Request to the default `master branch`  
Ref.: https://www.attosol.com/create-and-merge-branches-using-github-desktop-client/  

#### Test that the changes are applied live in production  
Open a browser and type https://username.github.io  
*It can takes up to 10 minutes for GitHub Pages to build your site and display your changes live
**Don't forget to clear your local browser cache as well ;)

### Keep local environment synced with GitHub-Pages Gem  
Edit Gemfile  
Comment this line:  
`# gem "jekyll", "~> 3.7.3"`  
Uncomment this line:  
`gem "github-pages", group: :jekyll_plugins`

### Add pertinent supported GitHub-Pages plugins

Ref.: [https://help.github.com/articles/configuring-jekyll-plugins/](https://help.github.com/articles/configuring-jekyll-plugins/){:target="blank"}  
[https://help.github.com/articles/adding-jekyll-plugins-to-a-github-pages-site/](https://help.github.com/articles/adding-jekyll-plugins-to-a-github-pages-site/){:target="blank"}  

#### Site Map

Edit _config.yml file  
Add this line:
~~~
- jekyll-sitemap
~~~  
Edit Gemfile
Add this line:
~~~
gem "jekyll-sitemap"
~~~  
  
#### SEO
Edit _config.yml file  
Add this line:
~~~
- jekyll-seo-tag
~~~  
Edit Gemfile
Add this line:  
~~~
gem "jekyll-seo-tag"  
~~~  
Edit /_includes/head.html to add the SEO tag  
Ref.: [https://github.com/jekyll/jekyll-seo-tag#usage](https://github.com/jekyll/jekyll-seo-tag#usage)

### Setup to customise Minima theme

Open a browser and go to the theme repo https://github.com/jekyll/minima  
Download the repo on your computer  
Copy all the folders below, or the files you want to modify, to the root of your Jekyll folder on your computer

	_includes
	_layouts
	_sass
	assets

Ref.: https://help.github.com/articles/customizing-css-and-html-in-your-jekyll-theme/  
https://github.com/jekyll/minima#customization

### Add Bootstrap 4 using BootstrapCDN and local SASS

***To be completed***

Ref.: [https://getbootstrap.com](https://getbootstrap.com)  
[https://www.bootstrapcdn.com](https://www.bootstrapcdn.com)
[https://getbootstrap.com/docs/4.0/getting-started/introduction/](https://getbootstrap.com/docs/4.0/getting-started/introduction/)


### Add Favicons
Create the files `favicon.png`@ 72dpi 196x196px and `apple-touch-icon-precomposed.png`@ 72dpi 180x180px
Edit _includes/head.html and add thoses lines:  
~~~
<!-- Touch Icons - iOS and Android 2.1+ 180x180 pixels in size. --> 
<link rel="apple-touch-icon-precomposed" href="/apple-touch-icon-precomposed.png">

<!-- Firefox, Chrome, Safari, IE 11+ and Opera. 196x196 pixels in size. -->
<link rel="icon" href="/favicon.png">
~~~  

### Add Dynamic Copyright in the footer  
Edit /_includes/footer.html
Add this lines:
~~~
Copyright &copy; {{ site.time | date: '%Y' }} Copy Owner
~~~
Ref.: [https://michaelsoolee.com/jekyll-copyright/](https://michaelsoolee.com/jekyll-copyright/)

### Add Categories filter
Ref.: [https://blog.webjeda.com/jekyll-categories/#create-a-category-page](https://blog.webjeda.com/jekyll-categories/#create-a-category-page)

### Make blog post URLs SEO Friendly
Edit _config.yml and add this line:  
`permalink: /blog/:title/`  
Ref.: [https://jekyllcodex.org/without-plugin/pretty-permalinks/](https://jekyllcodex.org/without-plugin/pretty-permalinks/)

### Add Contact or any other Forms 
Create form handler with Brisk Forms
Open a browser and go to [http://briskforms.com/new](http://briskforms.com/new)
Provide a "Response Email" and a "Redirect" URL, click "Create"
Copy the content of the field: "Set your form's action attribute to:" Looking like this `http://briskforms.com/go/2daf6`
Edit any .md and/or _includes/*.html and/or _layouts/*.html files and add those lines (replace the "form handler" with the one copied):
~~~
<form method="post" action="https://briskforms.com/go/xxxxxxxxxxxxxxxxxxxxxxx">
	<h4> Contact </h4>
  <input type="name" name="name" placeholder="Name" required>
  <input type="email" name="email" placeholder="Email" required>
  <textarea name="message" placeholder="Message" required></textarea>
  <button type="submit">Send</button>
</form>
~~~  
*Change the provided address for `https` to have the form sent secure

### Add Comments on blog articles using Disqus  

Create account on [https://disqus.com](https://disqus.com)
Edit _config.yml and add those lines:
~~~
# Disqus Comments
disqus:
    # Leave shortname blank to disable comments site-wide.
    # Disable comments for any post by adding `comments: false` to that post's YAML Front Matter.
    shortname: mydisqusshortname
~~~
Create a file disqus_comments.html in _includes folder and copy thoses lines:  
```
{% if page.comments != false and jekyll.environment == "production" %}

  <div id="disqus_thread"></div>
  <script>
    var disqus_config = function () {
      this.page.url = '{{ page.url | absolute_url }}';
      this.page.identifier = '{{ page.url | absolute_url }}';
    };
    (function() {
      var d = document, s = d.createElement('script');
      s.src = 'https://{{ site.disqus.shortname }}.disqus.com/embed.js';
      s.setAttribute('data-timestamp', +new Date());
      (d.head || d.body).appendChild(s);
    })();
  </script>
  <noscript>Please enable JavaScript to view the <a href="https://disqus.com/?ref_noscript" rel="nofollow">comments powered by Disqus.</a></noscript>
{% endif %}
```
Edit _layout/post.html and add those lines at the end of the file:  
~~~
{% if site.disqus.shortname %}
  {% include disqus_comments.html %}
{% endif %}
~~~

*The comments will only load in production environment. Follow the instructions for [Running Jekyll in production environment localy](#running-jekyll-in-production-environment-localy) section bellow.  
Ref.: [https://sylvaind.disqus.com/admin/install/platforms/jekyll/](https://sylvaind.disqus.com/admin/install/platforms/jekyll/)  
[https://desiredpersona.com/disqus-comments-jekyll/](https://desiredpersona.com/disqus-comments-jekyll/)  
[https://github.com/jekyll/minima](https://github.com/jekyll/minima)  

### Setup Google Analytics

Note to myself: First, take a look at the file `_includes/google-analytics.html`

Open a browser and go to your [Google Analytics admin panel](https://analytics.google.com/)  
Setup a web property for your domain name
Generate a Tracking ID, copy it
Edit xxxxxxxx and paste the Tracking ID Script in the xxxxxx

Ref.: [https://stackoverflow.com/questions/17207458/how-to-add-google-analytics-tracking-id-to-github-pages?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa](https://stackoverflow.com/questions/17207458/how-to-add-google-analytics-tracking-id-to-github-pages?utm_medium=organic&utm_source=google_rich_qa&utm_campaign=google_rich_qa)  

### Setup a Custom Domain name

Go to your domain name provider  
Purchasse a domain (if you don't have one yet)  
Go to "Manage DNS"  
Enter 4 "A" and one "CNAME" reccords:
~~~
A @ 185.199.108.153 TTL 600 Seconds
A @ 185.199.109.153 TTL 600 Seconds
A @ 185.199.110.153 TTL 600 Seconds
A @ 185.199.111.153 TTL 600 Seconds
CNAME WWW username.github.io
~~~
Ref.:
[https://help.github.com/articles/troubleshooting-custom-domains/#dns-configuration-errors](https://help.github.com/articles/troubleshooting-custom-domains/#dns-configuration-errors) [https://hackernoon.com/how-to-set-up-godaddy-domain-with-github-pages-a9300366c7b](https://hackernoon.com/how-to-set-up-godaddy-domain-with-github-pages-a9300366c7b)

### SEO Improvment 
Use canonical tag inside the head tag to have the SEO boots linking the "pagename/" and "pagename/index.html"  
Edit _includes/head.html and add this line:  
`<link rel="canonical" href="{{ page.url | prepend: site.url }}">`

### Speed Optomisation

#### Minify the HTML
Download the compress.html file from [https://github.com/penibelst/jekyll-compress-html](https://github.com/penibelst/jekyll-compress-html)  
Move the file compress.html to your /_layouts/ folder
Edit default.html and add those lines at the begening  
~~~
---
layout: compress  
---
~~~
Edit _config.yml and add those lines:
~~~
compress_html:
  clippings: all
  comments: ["<!-- ", " -->"]
  endings: all
  ignore:
    envs: [local]
  blanklines: true
  profile: false
  startings: [html, head, body]

~~~
To change its setting, take a look at the documentation [http://jch.penibelst.de](http://jch.penibelst.de)  
*I have set `blanklines: true` to solve an issue with [Lunr.js](https://lunrjs.com) search feature. All other settings are the ones from the documentation.  
*To avoid braking other html script, replace all comment format like this `// Comments` of any new included html files by this structure`/* Comments */`

#### Use Cloudflare
Create an account on [cloudflare.com](https://cloudflare.com)
Folow the wizard guide until the end to pull your DNS and change your name server.  
  
Modify the following settings:  
  
Crypto  
  
Speed  
  
Caching  
  
Page Rules  

## Some Helful Tips

### Jekyll. 
#### Issue running jekyll serve command  
Try running this command instead  
`bundle exec jekyll serve` or with the drafts published `bundle exec jekyll serve --drafts` 

#### Running Jekyll in production environment localy  
*Perfect to test Disqus comment
`JEKYLL_ENV=production bundle exec jekyll serve`
To build it and run it using another local web server use instead  
`JEKYLL_ENV=production bundle exec jekyll build`

#### To force running with Local environment setup
`JEKYLL_ENV=local bundle exec jekyll serve`

#### Jekyll fail to build after a change in _config.yml
Use spaces instead of tabs for the indentation should solve the issue. 

### Mac OSX
#### Show Mac hidden files   
shortcut on OSX `CMD + SHIFT + .`  

#### Run local web server using Phyton
In a terminal, navigate to the folder you want and type this command  
`python -m SimpleHTTPServer 8000`
Open a browser and type: [http://0.0.0.0:8000/](http://0.0.0.0:8000/)
To stop it, in Terminal press: `CTRL + C`

### Git

#### Install Git Command Line
From GtiHub Desktop  
Go to menu GitHub Desktop/Install Command Line Tool...

From Terminal  
Run `brew install git`  
Ref.:[https://git-scm.com](https://git-scm.com)   [https://gist.github.com/derhuerst/1b15ff4652a867391f03#file-mac-md](https://gist.github.com/derhuerst/1b15ff4652a867391f03#file-mac-md)  
  
#### Stop tracking Mac system files on the Git repo
Add system files to .gitignore  
Edit .gitignore file and add those lines:  

	.DS_Store
	._.DS_Store
	**/.DS_Store
	**/._.DS_Store

#### Delete all commit history on the Git repo  
1. Checkout  
`git checkout --orphan latest_branch`
2. Add all the files  
`git add -A`
3. Commit the changes  
`git commit -am "commit message"`
4. Delete the branch  
`git branch -D master`  
5. Rename the current branch to master  
`git branch -m master`
6. Finally, force update your repository  
`git push -f origin master`  

Ref.: [https://stackoverflow.com/questions/13716658/how-to-delete-all-commit-history-in-github](https://stackoverflow.com/questions/13716658/how-to-delete-all-commit-history-in-github)  

#### Reset the branch to a certain commit
1. Go to the branch you want to perform the action on
`git checkout master`    
2. Reset to the desired commit
`git reset --hard <commit number>`  
3. Force the push of this reset to the origin of the branch  
`git push -f origin master`  
4. If needed, repeat 1, 2 and 3 for the local branches as well  


[https://github.com/join]: https://github.com/join