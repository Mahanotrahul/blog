---
layout: post
title: Why I chose Jekyll?
date: 01/04/2024
description: Jekyll for static site generator for my blog
category1: Code
---

This was in the summer of 2020 during covid lockdown that I decided I wanted to have a website of my own. Being a website developer in college, I had a decent working knowledge of the basics - HTML, CSS, Javascript and a bit of JQuery. I researched through some online freely available website templates which I did not like. I wanted something really simple and minimalistic. That's when I stumbled upon Jekyll. [Jekyll](https://jekyllrb.com) is a static site generator, an open-source tool for creating simple yet powerful websites of all shapes and sizes. From [the project's readme](https://github.com/mojombo/jekyll/blob/master/README.markdown):

  > Jekyll is a simple, blog aware, static site generator. It takes a template directory [...] and spits out a complete, static website suitable for serving with Apache or your favorite web server. This is also the engine behind GitHub Pages, which you can use to host your project’s page or blog right here from GitHub.

It's an immensely useful tool and one we encourage you to use here with blog.
\
\
\
What intrigued me most of this is it was free to use and can be easily hosted in github pages. That means I could be running my website in a day or two. Github Pages already provides us with a free to use <username.github.io> URL that I could make use of. But I was slightly hesitant to start using this tool for the reason that I do not like to work with a tool that is not a industry standard, even though Jekyll was quite popular at the time, well it still is, and attaching a website to a tool meant if I wanted to move it to a different service someday, maybe to a cloud provider that didn't support Jekyll, I would have to go through the troubles of designing the application from scratch. However, this worry was resolved when I found that Jekyll also generates a _site folder in my local development that I could use to host my website with any cloud service provider. I don't have to rely on any whether or not Jekyll is supported by the cloud provider. This also meant I could run these static pages behind an nginx server on a VM somewhere in the cloud. This did it for me. I started my Jekyll journey but It was not an easy one.
\
\
Although Jekyll is quite easy to learn, customising and learning a new templating language - liquid was quite a headache for me at first. Once I had understood how it works, from then it was a piece of cake. I quickly developed a small website and hosted it on github with the github pages provided url mahanotrahul.github.io. Within the next couple of days, I had my website and a blog up and running.

After a break of almost 4 years, when I had been living in London for over a year, I wanted to redesign my blog - add a few more stories to it, add a light/dark theme switcher and update my pictures. The pictures I had were from 2017 lol so those definitely needed some updates. I looked very different from what I looked 7 years ago. Much older and yet still a kid at heart. Jekyll didn't have any native dark/light theme switcher support. While going through many blogs online, I really liked how few developers maintained their websites. Some were simple and minimal, some messily designed yet full with loads of information. I searched and found out that css itself now supports media queries to choose theme. For example, I could do

```css
html, html[data-theme="dark"] {
	--link-color: rgb(0, 0, 0);
}

html[data-theme="light"] {
	--link-color: rgb(129, 129, 129);
}

@media (prefers-color-scheme: dark) {
    html, html[data-theme="dark"] {
      	--link-color: rgb(0, 0, 0);
    }

    html[data-theme="light"] {
		--link-color: rgb(129, 129, 129);
    }
}
```

This is how one can create variables in css. So many years of knowing CSS and yet I had no idea we can do that lol. Anyhow, this was easy to understand. Now the `--link-color` variable can be assigned to the actual css property and boom, you can change the colors of css elements based on the user's system theme. I quickly added all these variables and created a button that will also changing the theme of the page. That worked perfectly. That how my website looks now. It's not perfect for sure. There is always scope for improvement but I like it nonetheless. Hope you like it too. Byee!

Find out more by [visiting the project on GitHub](https://github.com/mahanotrahul/blog).
