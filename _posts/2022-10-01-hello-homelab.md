---
title: Hello HomeLab
date: 2022-10-01 23:05 -400
categories: [homelab, hardware]
tags: [servers,dell]
---

# Welcome
This site will document the configuration of the servers / software that I'm using in my home lab environment.

I'm currently using the Jekyll static site generator as recommended by [Techno Tim](https://www.youtube.com/c/TechnoTimLive) on Youtube.

To start the local server to view changes to the posts on your development machine, use the following command at the bash prompt:
~~~bash
bundle exec jekyll s
~~~

## Hosting - Github Pages

If the site is being hosted on Github pages, all you need to do is commit the changes to your repository and then push the changes to Github.  The Github workflow will then process the changes and will automatically deploy the site.

~~~bash
git add .
git commit -m "feat(post) Describe this change"
git push
~~~

## Hosting - Locally

To build the site on the local file system, use this command:
~~~bash
JEKYLL_ENV=production bundle exec jekyll b
~~~
This will output the production site to the _site folder.  This files can then be served up by a web server either running on the machine or in a Docker container.

An example of this would be to create a Dockerfile to start up nginx:
~~~dockerfile
FROM nginx:stable-alpine
COPY _site /usr/share/nginx/html
~~~
Then build the image:
~~~bash
docker build .
~~~
If you don't want to use Docker, you could always copy the _site folder to an appropriate folder on an existing web server.  Since the filies are standard HTML/JavaScript, the web server does not need to have a database or have other dependencies.
