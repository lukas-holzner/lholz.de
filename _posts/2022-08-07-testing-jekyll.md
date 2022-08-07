---
title: "Testing Jekyll"
categories:
  - Blog
tags:
  - git
  - blog
---

I was searching for a way to have a small blog website to post projects to and where i can commit the posts to GitHub.

## What i found

After googeling, I found several repositories, with markedown files and example sites, which i later found out were all diffrent Themes for Jekyll. Next I found the GitHub documentation for Github pages, which also talked about Jekyll. That made me wanna try it. So i created a repository and started trying.

## Getting started

First i tried, a default theme called hacker. It was okay but not what i was searching for. next I found this custom theme called [Minimal Mistakes](https://github.com/mmistakes/minimal-mistakes) they had a very nice demo site, where they also posted their own posts, so i could really see it in action.

### Custom Domain

I am hosting this website on Github Pages. This is awsome. But of course i wanted to use my own domain for this website. fortunatly I can do so. I just ad to set `A` and `AAAA` records for the root domain lholz.de and a `CNAME` for *www.lholz.de*. I am using Cloudflare for my DNS, so this was an almost instantanous change. Unfortunatly I still have to wait 24 hours to be able to activate HTTPS.

## Testing Features

One of Minial Mistakes [Blog Posts](https://mmistakes.github.io/minimal-mistakes/layout/uncategorized/layout-header-video/) talks about adding videos anywhere in the text, by using this Liquid templateing code:

```liquid
{% include video id="BBnomwpF_uY" provider="youtube" %}
```

In this case, i can embedd a video, from one of my favourite Youtubers Jeff Geerling, without complicated html code, which might breake the look and feel of this post.

{% include video id="BBnomwpF_uY" provider="youtube" %}

Inclouduing Pictures, can be done, by uploading them into an assets folder, but I'm not really satisfied with that solution yet. I'll see if I can find something better.

## Conclusion

All in all, i am quite satisfied with this solution and it seems to be a far better option than Wordpress.