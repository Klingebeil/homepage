---
layout: post
title: "Building a new website"
date: 2021-03-10
teaser-img: 2021-03-20-teaser.png
---

It‘s been some time since I last updated my website or even published something on it. With platforms such as _Medium_, _Substack_ and _Revue_ taking over so much of the written indie-web, I didn’t see the need to take care of my own digital space.

But things change. Thought I will still use _Revue_ extensively to write and publish my (German) newsletter, I wanted to take a step back from _Medium_. _Medium_ is a seductive place. It‘s easy to use, has an in-build audience and you might even earn some money on the platform. (I earned at least enough to buy myself a cup of coffee this year.) So why change? Why build my own digital place?

Well, there are a couple of reasons.

1. For control—I want to have complete control over the things I publish; from design to format. Also f#ck the monopoly-platform-play.
2. To learn—A rather obvious one, but I wanted to challenge myself again.
3. To build—My job mostly happens inside Google Docs, over a cup of coffee and through lots and lots of talking. I like it that way, but I wanted to get my hands at least somewhat dirty and build something again for a change.

And with more time on my hand, than I would have liked (thanks Covid-19), I decided to finally tackle this project.

Form the start I knew, I wanted a couple of things my website should do:

- A place to publish blog posts
- A place that works as a portfolio for my projects
- A digital garden (I get to that in a minute)

{% include img-full.html id="2021-03-10-01.jpeg" alt="" info="The Money Shot" %}
## The Stack

In the end my choice fell on _Github_ Pages as a quick and easy platform after being inspired to check it out by Tom Critchlow’s piece [on his own digital garden](https://tomcritchlow.com/2019/02/17/building-digital-garden/) (yes, yes… let me finish here).

_Github_ Pages uses a programing language called _Jekyll_ to weave together blocks of _HTML_, _Markdown_ and _CSS_ to static pages. So, it‘s not fancy and quite bare-bones, but it has a couple of neat upsides for me and my workflow:

- I have been using _Ulysses_ for some time now to collect my notes and write articles. _Jekyll_ allows me to keep the workflow and just push slightly changed markdown files onto _Github_.
- _Jekyll_ also uses folders and files instead of other more opaque databases. So the whole site is extremely portable and backup-able. At the moment the whole side exists as a somewhat offline backup on my _Google Drive_. And I can simply push an update via Git to the online version. Neat and simple, once you get the hang of it.
- It also allows me to build lots and lots of custom designs and layouts. _Jekyll_ is really flexible in this way and allows me to do lots of hard-coded manipulations and tweeks on the go, once you‘ve set up your templates right.
- Also: I hate the _Wordpress_ editor with a passion.

## Planting a Digital Garden

Okay, what‘s a digital garden? To be concise, a digital garden is a collection of [^1]. It works similar to a personal wiki, where I can build on ideas while also being able to reference them quickly through links. Or as Tom Crithlow describes it:

> It’s a less-performative version of blogging – more of a captain’s log than a broadcast blog. The distinction will come down to how you blog – some people blog in much the same way. For me however blogging is mostly performative thinking and less captain’s log. So I am looking for a space to nurture, edit in real time and evolve my thinking.

Again I looked a Tom‘s [own digital garden](https://tomcritchlow.com/wiki/) for inspiration and lifted some of his Jekyll code from his _Github_, as well. (Sorry, Tom!)

It works again by using HTML- and markdown-files in folders, sorted by topic. The code loops through every single folder and collects the content on the main wiki-page, as well es every topic-page. Jekyll also creates a page for every note in the folder, which means I can simple link to single notes via URL.

So, if I want to update a file, I can simply jump into _Ulysses_, edit the content and then push the updated file back onto _Github_. No need for a complex and slow backend. Yes _Wordpress_, I am looking at you.

So yes. Here we are. New website, new system, lot‘s of room to play.

[^1]:	If you‘d like to read more, Patrick Tanguay published [a great overview on the different approaches and idaes behind digital gardens](https://sentiers.media/dispatch-08-digital-gardens/).