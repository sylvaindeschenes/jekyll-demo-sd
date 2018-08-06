---
layout: post
title:  "My Jekyll Static Website Features Checklist"
date:   2018-03-28 10:00:00 -0400
categories: Web-Development
comments: false
---
## Here is my wish list of features to be implemented on my Jekyll Website

### Implemented features  
*** 

#### General
- Responsive
- favicon  
- Menu to other Pages
- SEO frindly URL/permalink 
- Bread crump
- Contact Form
- Search site content
- Blog and post
- Limit number of post listed
- Category filter (basic)
- Discus Comments
- Newsletter creation (https://sylvaindeschenes.github.io/newslettertemplate/)
- Copyright (dynamic)
- Privacy Policy and T&C pages
- Profile Social icons
- Sitemap.xml (for SEO robots)

#### Text
- Anchors
- Paragraph expend
	
#### Medias
- Pdf document
- Open external links and pdf in new window
- Image
- Video
- Image and video Lightbox
- Embed video and MP3 
- Image Gallery
- Image Lazy Loading

### To be implemented 
*** 

#### General
- Replace site title by a logo
- Multilingue
- User site map (displayed or link in footer)
- Google Analytics (check Minima config + [https://jekyllcodex.org/without-plugin/metrics/](https://jekyllcodex.org/without-plugin/metrics/). 
- Click tracking [bitly](https://bitly.com)
- [Conversion Pixel Facebook](https://www.facebook.com/business/help/952192354843755)
- [Conversion Tracking AdWords](https://support.google.com/adwords/answer/6095821)
- Newsletter (Mailchimp or Tinyletter)

#### System
- Custom domain name 
- Cloudflare account
- Pingdom account
- [CouldCannon CMS](https://cloudcannon.com) 

#### Page Design  
- Add background image
- Menu to scroll down on the Home Page Sections  
- Home Page Paralaxe
- Timeline  
- Project/Portfolio Gallery / Sub-Gallery Photo Video  
- Action button
- Action Banner
- Scroll Top Button  
- Phone (phone number format) and Address
 
#### Blog Articles
- Pagination with previous-next buttons
- Show Related posts
- Category filter (better UI/UX - advanced)

#### Others
- Live Chat [https://crisp.chat](https://crisp.chat)
- eCommerce  [https://jekyllcodex.org/without-plugin/webshop/](https://jekyllcodex.org/without-plugin/webshop/)
- Adds

#### Speed Optimisation
- See my bookmark ;)

### Copywriting et images
*** 
- Site logo + New Favicon.png
- Terms & Conditions and Privacy Policy

- Fix code block formatting in 2018-03-29-how-to-build-a-static-website-using-jekyll-on-github-pages.md sections:  
-- Disqus comment section  
-- Add  Dynamic Copyright in the footer section  

- Is Canonical well set automaticaly on Jekyll or do I need to add this
~~~
	<!-- Use canonical tag inside your head tag to have the SEO boots linking "pagename/" and "pagename/index.html" -->
	<link rel="canonical" href="{{ page.url | prepend: site.url }}">
	<link rel="canonical" href="{{ site.url }}{{ page.url | replace:'index.html',''}}">
~~~
