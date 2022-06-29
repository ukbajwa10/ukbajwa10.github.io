---
layout: post
title: Virtual Home Lab + My New Blog
date: 2022-03-12 14:06:30 -0600
categories: technology
---

Beside my main computer I have a Dell Poweredge server and an HPE ProLiant DL360 server, and to be completely honest with you, I hate them both (sorry Joel). They're loud, clunky, attract so much dust, and it's a pain to set them up with a monitor. I actually built a server rack to put the DL360 in but it's been living permanently on my patio. 

## Here's what I did to setup my virtual lab: 

- I installed virtualbox and downloaded a preconfigured virtualbox image from osboxes.org, these are really useful. I went with CentOS just because I want to learn RHEL but Ubuntu is really linux beginner friendly. 
- It might have just been me but my network connection was not enabled by default. If you have any issues with that, here's the article <https://superuser.com/questions/915536/centos-7-virtualbox-no-internet-access> I used to troubleshoot it, specifically the answer by "Rafael15986".  
- For my cloud provider, I'm learning Azure. I'm using a free account but I'm still worried about runaway cloud costs. A friend of mine recommended I learn Terraform for easy resource destruction, he also said using "terraform destroy" makes him feel like a badass so I'm already convinced. I'll probably make my next post about that.

## For this blog:

I followed a guide for setting up Jekyll and Ruby on CentOS and then using git I pushed my changes to production. I decided on Jekyll because it's super simple to set up, you literally just need to install Ruby and Jekyll. I was doing the above at first but when I was looking at jekyll themes I found something much simpler. You can just fork this repo on Github: <https://github.com/barryclark/jekyll-now>, I realized it's just way easier to edit things on github and commit, despite how cool it is to use git commit and git push in bash. 

But I decided to take things a step further. Originally, I had my blog setup using only github pages, you can set these up for free on the site: username.github.io, so you can actually still see mine at <ukbajwa10.github.io>. But, since I'm learning Azure, I wanted to implement in Azure cloud. I created a Static Web App in Azure, I had a lot of trouble with it at first but then discovered you NEED to add Jekyll as an environment variable in the yaml workflow file. I then bought this domain from porkbun, configured the DNS in the Azure portal, and now I'm all set. What's really cool about this method is that the Azure Web App automatically pulls any changes I make on Github and pushes them to production. 



## Sources: 

Blog Setup
  - <https://docs.github.com/en/pages/setting-up-a-github-pages-site-with-jekyll/creating-a-github-pages-site-with-jekyll>
  - <https://www.rubyguides.com/2018/09/ruby-gems-gemfiles-bundler/>

Static Web App: 
  - <https://docs.microsoft.com/en-us/azure/static-web-apps/publish-jekyll>
  - <https://docs.microsoft.com/en-us/azure/static-web-apps/custom-domain>

Domain Registrar:
  - <https://porkbun.com/>
