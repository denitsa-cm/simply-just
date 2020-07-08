---
layout: post
title: Hello World!
categories: [general]
tags: [hello, new blog]
fullview: true
comments: false
description: New blog with Jekyll on Github Pages
date: 2020-07-08 07:59:00 +0200
---

I thought it would be fun to try keeping a blog and test out a static site generator like Jekyll, hosted on Github Pages.

I'm not at all familiar with the pros and cons of all static site generator, so my choice was pretty random - I just googled something and this seemed popular. 
I thought it looked simple enough to set up (and it sort of was), but it still took me about an hour or two to get a theme going.

I looked through [Jekyllthemes](https://jekyllthemes.io/) and thought [Dbyll](https://jekyllthemes.io/theme/dbyll) looked nice for a starter theme.
To be honest, I liked [Balzac](https://jekyllthemes.io/theme/balzac-for-jekyll) at first, but I got stuck in the setup process. I bet there was something wrong
about my `_config.yml` file that I probably could fix now with my new knowledge from the last hour. 

In any case, I'm going with the Dbyll theme for now. I made a few small adjustments, like removing the avatars on the left and under each blog post until I find an image I want to use.

As a newbie, I had a few hickups during the setup of the Dbyll theme, so here they are in case anyone encounters the same:

1. Site was working locally with `bundle exec jekyll serve` but not when deployed to Github pages. 
I figured out (by looking at the code and some old PR into the theme repo), that I have to set the `BASE_PATH: /my-github-repo` in `_config.yml`. That's probably obvious, but it wasn't for me as a person who's never seen Jekyll before :)
I also set `url: {github_user}.github.io` and `baseurl: /my-github-repo` (I read it somewhere and wanted to be on the safe side). 

2. The other thing I did was add the `gem 'github-pages'` to the Gemfile, cause that's supposedly the thing you need to deploy to github pages (I haven't tested if it works without it yet).

3. Then I could still not get any of the sample posts inside `_posts` to load on the home page. Looked up the docs for the paginator and my posts started appearing after adding a `paginate: 5` to `_config.yml`