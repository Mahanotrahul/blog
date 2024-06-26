---
layout: post
title: Why I chose Jekyll?
date: 01/04/2024
description: Jekyll is a static site tool used to develop for my blog
category1: Code
---

This was in the summer of 2020 during covid lockdown that I decided I wanted to have a website of my own. Being a website developer in college, I had a decent working knowledge of the basics - HTML, CSS, Javascript and a bit of JQuery. I researched through some online freely available website templates which I did not like. I wanted something really simple and minimalistic. And also working with a pre decided template is really difficult as it is hard to understand the classes and id's it uses to style the page.\
I also wanted a template based solution that could be used for a blog. I have always been interested in writing a blog and stories about things that seem even mildly interesting to me. That's when I stumbled upon Jekyll. [Jekyll](https://jekyllrb.com) is a static site generator, an open-source tool for creating simple yet powerful websites of all shapes and sizes. From [the project's readme](https://github.com/mojombo/jekyll/blob/master/README.markdown):

  > Jekyll is a simple, blog aware, static site generator. It takes a template directory [...] and spits out a complete, static website suitable for serving with Apache or your favorite web server. This is also the engine behind GitHub Pages, which you can use to host your project’s page or blog right here from GitHub.

\
\
\
What intrigued me most of this is it was open source, free to use and can be easily hosted in github pages. That means I could be running my website in a day or two. Github Pages already provides us with a free to use <username.github.io> URL that I could make use of. But I was slightly hesitant to start using this tool for the reason that I do not like to work with a tool that is not a industry standard, even though Jekyll was quite popular at the time, well it still is, and associating a website to a particular tool meant that if I wanted to move it to a different hosting service someday, maybe to a cloud provider that didn't support Jekyll, I would have to go through the troubles of designing the application from scratch. However, this worry was resolved soon when I learned that Jekyll also generates a _site folder in my local dev environment with all the static files that I could use to host my website with any cloud service provider. I don't have to rely on any whether or not Jekyll is supported by the cloud provider. This also meant I could run these static pages behind an nginx server on a VM somewhere in the cloud. This did it for me. I started my Jekyll journey from thereon but It was not an easy one.
\
\
Although Jekyll is quite easy to learn, customizing and learning a new template language - liquid was quite a headache for me at first. Once I had understood how it works, from then it was a piece of cake. I quickly developed a small website and hosted it on github with the github pages provided url mahanotrahul.github.io. Within the next couple of days, I had my website and a blog up and running.

After that I got so busy with my collee and Job soon after that I couldn't really spend much time updating the site. In 2022, I bought this domain - <rahulmahanot.in>. I used godaddy to buy the domain and moved the nameserver's over to Cloudflare so I can utilize the amazing features provided by this awesome website.
In 2024, after spending my time in London and working at Apple for just over a year, I decided to take up the task of blogging again. After a break of almost 4 years since I designed my first blog site, I wanted to redesign my blog - add a few more stories to it, add a light/dark theme switcher and update my pictures. The pictures I had added in the first iteration were from 2017 lol so those definitely needed some updates. I look very different in 2024 from what I used to look like 7 years ago. Much older and yet still a kid at heart 😜. Jekyll didn't have any official native dark/light theme switcher support. While going through many blogs online, I really liked how few developers maintained their websites. Some were simple and minimal, some messily designed yet full with loads of information. I searched and found out that css itself now supports media queries to choose theme. For example, I could do

```css
html, html[data-theme="dark"] {
	--link-color: rgb(129, 129, 129);
}

html[data-theme="light"] {
	--link-color: rgb(0, 0, 0);
}

@media (prefers-color-scheme: dark) {
    html, html[data-theme="dark"] {
      	--link-color: rgb(129, 129, 129);
    }

    html[data-theme="light"] {
		--link-color: rgb(0, 0, 0);
    }
}
```

This is how one can create variables in css. So many years of knowing and head scratching with CSS and yet I had no idea we can create variables in CSS lol. This was easy to understand. Now the `--link-color` variable can be assigned to the actual css property like so
```css
  body {
    color: var(--link-color);
  }
```

and boom, we can change the colors of css elements based on the user's selected theme. If the user chooses light theme, color changes accordingly to `rgb(0,0,0)` and when dark theme is selected, color changes to `rgb(129, 129, 129)`. I quickly added all these variables and created a button that will also change the theme of the page. That worked perfectly. That's how I added a theme-switcher to my website. Hope you like it.\
Let me know if you would like to know more about me or want to have a chat with me. Byee!

Find out more by [visiting the project on GitHub](https://github.com/mahanotrahul/blog).
