---
layout: post
title:  "Working with Draft posts"
date:   2018-03-28 11:21:55 -0400
categories: jekyll update
---
## Working with _drafts posts

In Terminal run `jekyll serve --drafts`

Ref.: https://jekyllrb.com/docs/drafts/

### Notes

- If the post's date is in the future. You can make the post visible by setting `future: true` in `_config.yml`

- If the post has `published: false` in its front matter, it will not show up. Set it to `true`.

Ref.: https://stackoverflow.com/questions/30625044/jekyll-post-not-generated

## Markdown cheatsheet

https://www.markdownguide.org/cheat-sheet

### Below is the default Minima post:

You’ll find this post in your `_posts` directory. Go ahead and edit it and re-build the site to see your changes. You can rebuild the site in many different ways, but the most common way is to run `jekyll serve`, which launches a web server and auto-regenerates your site when a file is updated.

To add new posts, simply add a file in the `_posts` directory that follows the convention `YYYY-MM-DD-name-of-post.ext` and includes the necessary front matter. Take a look at the source for this post to get an idea about how it works.

Jekyll also offers powerful support for code snippets:

{% highlight ruby %}
def print_hi(name)
  puts "Hi, #{name}"
end
print_hi('Tom')
#=> prints 'Hi, Tom' to STDOUT.
{% endhighlight %}

Check out the [Jekyll docs][jekyll-docs] for more info on how to get the most out of Jekyll. File all bugs/feature requests at [Jekyll’s GitHub repo][jekyll-gh]. If you have questions, you can ask them on [Jekyll Talk][jekyll-talk].

[jekyll-docs]: https://jekyllrb.com/docs/home
[jekyll-gh]:   https://github.com/jekyll/jekyll
[jekyll-talk]: https://talk.jekyllrb.com/
