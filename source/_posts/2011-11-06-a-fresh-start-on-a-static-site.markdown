---
layout: post
title: "A Fresh Start on a Static Site"
date: 2011-11-06 10:18
comments: true
categories: 
---
I've decided to move my blog to a new domain and use a static site
generator to serve up the content. Since the content doesn't change
much, it makes little sense to continue using Wordpress on a shared
web hosting plan with limited resources.

## Static Sites Are Fast
A static site significantly reduces the overhead of disk I/O by 
taking the relational database out of the picture. Most modern web
servers can be highly tuned to avoid disk access for static content by
utilizing output caching. If setup correctly, the fast majority 
of web requests require zero disk I/O. This allows the web server to
serve content faster and handle larger loads with less resources.

While it is possible to use Wordpress Plugins like SuperCache to reduce
disk I/O, it still requires a Fast CGI process to serve the content via 
PHP. This incurs enough CPU usage to make it slower than a pure static site.

## Easy cloud based hosting and scaling
While a typical shared hosting setup works most of the time, it
does carry the possibility of a popular post bringing your hosting
to its knees. Planning for this kind of event carries a lot of 
cost which will go unused most of the time.

Cloud based hosting platforms, like <a href="http://www.heroku.com">Heroku</a>,
are perfectly suited for hosting static sites that can be scaled up very easily.
Heroku's free plan goes a long way and would likely handle the vast majority of
traffic, but still give you the ability to use push button scaling for those rare
instances when a post hits the #1 page of <a href="http://news.ycombinator.com">Hacker News</a>

## Choosing a static site generator
There a number of static site generators that will perform the basic
operations of translating posts that are written in
<a href="http://daringfireball.net/projects/markdown/">Markdown</a>
into HTML and organizing the output along with any uploaded media.

I chose to go with <a href="http://octopress.org">Octopress</a> because it
offered the following:

* Ruby based and easily customizable with plugins.
* Easily configured to work with Heroku.
* Stylesheets are written in <a href="http://thesassway.com/">Sass</a>.
* Excellent typography out of the box with the base theme.
* Sits on top of <a href="http://github.com/mojombo/jekyll">Jekyll</a>, and 
can utilize many existing plugins.
* Easy local preview with a built in Rack server.

## Migrating old content
I've chosen to move my old wordpress install over to wordpress.com's
free plan for archival purposes rather than attempt a content migration.
But if you want to preserve your old content and links, there is a
Wordpress to Jekyll migrating tool called 
<a href="http://github.com/thomasf/exitwp">ExitWP</a> that many have used
successfully. Also, you can utilize a rack server to execute code to handle redirects.

## Additional Resources
* <a href="http://inessential.com/2011/03/16/a_plea_for_baked_weblogs">A plea for baked weblogs</a>
* <a href="http://mattgemmell.com/2011/09/12/blogging-with-octopress/">Matt Gemmell's post on blogging with Octopress</a>
* <a href="http://www.scottw.com/moving-to-octopress">Scott Watermasysk's post on Octopress with Heroku</a>

