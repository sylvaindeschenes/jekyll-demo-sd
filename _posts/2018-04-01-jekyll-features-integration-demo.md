---
layout: post
title:  "Jekyll Features Integration Demo"
date:   2018-04-01 10:00:00 -0400
categories: Web-Development
---

## All the features I have integrated to this site, that can be demoed visually, are displayed on this blog article

I'm using this page to demo all integrated features on this website and reuse them on the site's pages and posts when needed. All those features are integrated WITHOUT PLUGIN to keep Jekyll ability to be built by GitHub Pages.

### Buttons ***To be improved***

<button type="submit">Action Button</button> Triger nothing at the moment

### Search the website using [Lunr.js](https://lunrjs.com) from [Jekyll Codex](https://jekyllcodex.org/without-plugin/buttons/)

{% include search-lunr.html %}  

### Contact Form and other forms from [Jekyll Codex](https://jekyllcodex.org/without-plugin/form-builder/) ***To be completed***

[Advanced Contact Form]({{ "/contact" | absolute_url }})  
*Form builder (form.html) and Better forms (better-forms.html) are installed but the form is not sending yet

### Newsletter template from [idratherbewriting.com](http://idratherbewriting.com/2016/10/23/jekyll-newsletter-tip/)

[Newsletter template]({{ "/newslettertemplate" | absolute_url }}){:target="_blank"}

### Ligthbox from [Jekyll Codex](https://jekyllcodex.org/without-plugin/lightbox/)   

[Video link using Lightbox](https://youtu.be/iWowJBRMtpc)

[Image using Lightbox]({{ "/assets/images/image-sample1.jpg" | absolute_url }})

[Video link using no-lightbox attributes](https://youtu.be/iWowJBRMtpc){:.no-lightbox} 

### Image gallery from [Jekyll Codex](https://jekyllcodex.org/without-plugin/image-gallery/)  

{% include image-gallery.html folder="/assets/gallery/album" %}  

### Youtube, Vimeo, MP3 links handled by Open embed from [Jekyll Codex](https://jekyllcodex.org/without-plugin/open-embed/) ***Parameters to fix***

Simple video link  

https://vimeo.com/channels/staffpicks/261794608

Video link with parameters ?autoplay=1&loop=1&controls=0&t=90s  

https://vimeo.com/channels/staffpicks/262628873?autoplay=1&loop=1&controls=0&t=90s

#### Tring to fix the parameters ?autoplay=1&loop=1&controls=0&t=90s

### Anchors to navigate throught the sections of a page or post

[Go to the section PDFs](#pdfs)  
[Go to the section Links](#links)

### Text expend from [Jekyll Codex](https://jekyllcodex.org/without-plugin/text-expand/)

This is a long paragraph that can be expanded Lorem ipsum dolor sit amet, consectetur adipiscing elit. Vivamus in neque non tortor congue cursus vel eu nibh. Integer suscipit vel felis a congue.

[expand]  
 
Lorem ipsum dolor diam a elit tempor dapibus. Integer vel nisi a nisi accumsan tristique ac sed metus. Nunc efficitur gravida nulla, in aliquam tortor placerat eget. Quisque varius augue non augue placerat elementum id non neque. Integer rutrum velit vel lectus tempus, nec pellentesque quam pellentesque. Duis tincidunt sagittis nisl sed semper. In venenatis neque tincidunt commodo lacinia. Aliquam quis volutpat metus. Nunc ipsum metus, convallis id pellentesque quis, semper a ipsum. Aliquam congue, quam vel lobortis fermentum, ante erat accumsan ex, quis bibendum metus purus non diam.  

[/expand]

### External links and PDF documents are open in a new window with New window fix from [Jekyll Codex](https://jekyllcodex.org/without-plugin/new-window-fix/)  

#### PDFs

[Link to an internal PDF]({{ "/assets/documents/mytest.pdf" | absolute_url }}) <--- Open in a new page/tab using New window fix  

[Link to an internal PDF - with traget Blank specified]({{ "/assets/documents/mytest.pdf" | absolute_url }}){:target="_blank"}   

#### Links

[Link](https://jekyllrb.com)  <--- Open in a new page/tab using New window fix

[Link with traget Blank specified](https://jekyllrb.com){:target="_blank"} 

[Link with traget Blank and NoFollow specified](https://jekyllrb.com){:target="_blank"}{:rel="nofollow"}   

### Auto-resize images using [Images.weserv.nl](https://images.weserv.nl) from [Jekyll Codex](https://jekyllcodex.org/without-plugin/auto-resize-images/) ***To be completed***

This is a full size image located at this link {{ "/assets/images/image-sample6.jpg" | absolute_url }} 

This is a sample image displayed in full size  

![Sample image displayed in full]({{ "/assets/images/image-sample6.jpg" | absolute_url }})  

### Lazy loading by  [Jekyll Codex](https://jekyllcodex.org/without-plugin/lazy-loading/)
 
<img src="/assets/siteimages/lazyload-blank.png" alt="" data-echo="/assets/images/image-sample1.jpg">  
<img src="/assets/siteimages/lazyload-blank.png" alt="" data-echo="/assets/images/image-sample2.jpg">  
<img src="/assets/siteimages/lazyload-blank.png" alt="" data-echo="/assets/images/image-sample3.jpg">  
<img src="/assets/siteimages/lazyload-blank.png" alt="" data-echo="/assets/images/image-sample4.jpg">  
<img src="/assets/images/image-sample17-lazyload.jpg" alt="" data-echo="/assets/images/image-sample17.jpg">  

Background image ***To be fixed***

<div style="background: url(/assets/siteimages/lazyload-blank.png) center center no-repeat; background-size: cover;" data-echo-background="/assets/images/image-sample13.jpg"></div>

### Comment from [Disqus](https://disqus.com) 
See below, at the bottom of this article.