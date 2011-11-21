---
layout: post
title: "An Open Source Workflow With Ruby on Rails"
date: 2011-11-21 09:21
comments: true
categories: 
---
I've been an advocate of open source for a long time. First via software 
that I used, like Mozilla's Firefox, and later though consuming open 
source code and contributing back to it. I've used open source code on a 
number of platforms over the years including PHP, Java, .NET, and Ruby on Rails.

Out of the platforms that I have used, I believe Rails has the most accesible open 
source ecosystem because it enables consumption and contribution better than most other platforms.

This post will be my attempt at describing a developer's work flow when using open source with Ruby on Rails.

## Discovery
The first step to consuming open source to use on a Rails project is 
discover existing open source libraries, called gems in Ruby, to 
solve a problem that you encounter while building your application. 

There are number of screencast sites, podcasts, and 
mailing lists out there that highlight useful gems and how to use them.
Here's a few that I use:

* Ryan Bates' Screencasts at [Railscasts](http://railscasts.com)
* [Ruby 5 Podcast](http://ruby5.envylabs.com)
* Peter Cooper's [Ruby Weekly](http://rubyweekly.com)

Most gems are hosted via [RubyGems.org](http://rubygems.org). This site also maintains a search index 
with links to source and documentation for any gems 
hosted there.

[GitHub](http://github.com) is also a good place to discover gems via search.

Some key criteria that I look for in a gem that I'm considering for use in a production 
application are the following:

- Publically Hosted on GitHub
- Recent commits within the last 3 months
- A high number of Forks/Watchers
- A low number of currently open Pull Requests.

These are just my personal guidelines, so feel free to relax them as you see fit. For side projects to hack on, 
you can (and should) be a lot more willing to try more experimental gems.

## Installing Gems with Bundler
Once you've identified a few gems that you'd like to use, the standard 
recommendation is to use [Bundler](http://gembundler.com) to manage your external gems. 

Bunder is a dependency management gem that uses a manifest file 
called a GemFile that lists out the gems in the root of your project. 

To add a dependency in the simplest way, edit your Gemfile 
and add a line similar the following line to add the Carrier Wave gem.

``` ruby GemFile for Carrier Wave
gem 'carrierwave'
```

Once you've updated your Gemfile, run 'bundle install' to have Bundler 
pull down your gems and install them for use in your app.

## Adjusting your versions
In the course of using your gem, you may find that you need to use a 
different version than the current version published on RubyGems.org.

To go back to an older published version of the gem, you can adjust your Gemfile 
like below.

``` ruby GemFile for Carrier Wave with version
gem 'carrierwave', '0.5.4'
```

After updating your GemFile, run 'bundle update <gemname>' to force 
Bundler to reinstall the gem using the correct version.

If you're feeling more adventurous, or simply want to test the most 
current code for the gem with your app, you can point directly to its 
public git repository by putting this in your GemFile.

``` ruby GemFile with git repo here.
gem 'carrierwave', :git => 'git://github.com/jnicklas/carrierwave.git' 
```

Finally, if you've cloned the gem's source code locally, you can point to a local directory for 
the gem here.

``` ruby GemFile with local directory here.
gem 'carrierwave', :path => "~/Projects/carrierwave/"
```

## Forking to fix
If you find that the gem you are using contains a bug, and the gem's 
code is on GitHub, it's very easy to attempt a bug fix and test it locally in 
your application.

The first step is to fork the gem's repository using your GitHub 
account.

{% img http://f.cl.ly/items/2Q1V0I160h3J241b2Q2B/jnicklas_carrierwave%20-%20GitHub.png %}

Then clone your fork locally.

``` plain
cd ~/Projects
git clone git@github.com:hkarthik/carrierwave.git
```

Next, point your application to your locally cloned Git repository for 
your fork of the gem which contains the bug.

``` ruby GemFile with cloned local directory here.
gem 'carrierwave', :path => "~/Projects/carrierwave/"
```

Now you're all set to edit your local clone of the gem and fix it.

If you're using your application to test your fix, you'll need to run 
'bundle update <gem name>' to rebundle the gem into your application 
whenever you make changes. 

Because this can sometimes be a slow process, I advise writing tests within the gem's source code first before 
bundling into your app for integration testing.

Once you've fixed the gem, you can commit your fix, and push to your fork on GitHub.

``` plain
git commit -am 'Fixing this gnarly bug'
git push origin master
```

Then you can modify your application's GemFile and point to your GitHub 
fork of the gem:

``` ruby GemFile with git repo of forked gem
gem 'carrierwave', :git => 'git://github.com/hkarthik/carrierwave.git' 
```

From here, you could continue to maintain your fork and keep it up to date 
with the latest changes from the original gem's repository. While you 
can certainly choose to go this route, I would recommend contributing 
back the fix with the eventual goal of deleting your fork.

## Contributing back
So now that you've fixed the code in the gem, you're back to cruising 
along on your app. Why not make the fix available for anyone else using 
the gem? GitHub makes this process easy.

Browse to your fork on GitHub and click the Pull Request button.

{% img http://f.cl.ly/items/2E0v1z2g3C2u1C1P1D0A/hkarthik_carrierwave%20-%20GitHub.png %}

Fill in some details about the fix you've made. Submit the pull request and wait for feedback from the 
project maintainers.  If they accept your pull request then your fix 
will make it into the master repository instantly.

If your fix is accepted and later incorporated in the next published 
version of the gem, I recommend moving your application back to the 
published gem and deleting your fork on GitHub.

While you can leave your fork out there, if you're not actively maintaining it, you're likely to confuse anyone else looking
for the source code of the gem. Unmaintained forks are just unnecessary
noise on GitHub, and I don't suggest keeping them around. 

## Conclusion
I hope this post gave you a good start on how to contribute to open source while 
building applications in Ruby on Rails.

You don't have to be an expert to start contributing to open source. 
All you need is the right tools and a little bit of knowledge on how to 
get started. It's a great feeling to watch your first pull requests get accepted into 
your favorite open source project and realize that you've just given back.

I've used a lot of open source in the past, but only recently have I 
felt confident enough to start contributing back. I'm glad I did, as it's great 
feeling to give back in some small way to projects that have saved me countless hours 
while building applications. I hope that I've inspired you to do the
same.
