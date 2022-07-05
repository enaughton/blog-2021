---
layout: layouts/post.njk
title: One month at Luro
date: 2022-07-05T13:43:46.866Z
tags:
  - Learning
---

I often forget to reflect on things I've learned. This year as a whole has been a rollercoaster of lessons and growth. 

Its been a month since joining [Luro](https://luroapp.com/).

So fair this what have I have learned


1. Vue

2. Nuxt

3. Prisma

4. Projects

5. Crawlers

6. Testing

7. Local Db

8. Document



## 1. [Vue](https://vuejs.org/)

First time using Vue, it just makes sense. It feels like I'm playing around in [codepen](codepen.io) all day.



No jumping around files, or moving to different parts of the file structure to find something that needs to be edited.



- Template

- Script

- Style



All in your stuff one file. You can arrange those however you like too! 



I think the most useful thing I've used so far is the `v-if` statements to be able to conditionally render different `templates` based on need.



## 2. [Nuxt](https://nuxtjs.org/)

Felt like magic, when getting the tour of Luro App.



With build in things like \`NuxtLink\` makes it very straight forward to create links.



In Nuxt there are two important methods for fetching data

`asyncData` for data required to successfully render the page. Render blocking and has

`fetch` for lazy-loadable data.

We use `$axios` to fetch everything. We are waiting on Nuxt 3 in favor of `useFetch()` or `$fetch`.



## 3. [Prisma](https://www.prisma.io/)

Another tool that I am very excited about.

Prisma actually made the first big feature I built for Luro, very straight forward. I had to add one line to the Prisma file, and hit the ground running.


There is much more to learn here, so far I've learned

- `npx prisma studio` (a view of your database)

No complaints about prisma. Very helpful to quickly be able to build stuff. I want to learn more about it, and to be able to be more helpful with backend tasks.



## 4. Projects

This was the big feature that I helped build out in my first week.

Prisma made it very easy to build this out, just by adding one line of code in the ORM.

Then it was all about just making the UI work properly. 



## 5. Page Crawlers

I also learned about page crawlers and how to make adding pages from a crawled website to our database.

Building out the views and templates for this feature was challenging because of all the moving parts.

We have to crawl the URL for different pages, return those pages back to the user. Let the user select which pages they want to add.

Take screenshots of the crawled pages using puppeteer. Then display all those pages on `/pages`


This requires loading states, and getting conditionally rendered views back to the user.



Then to make sure it all fit in modals and worked properly. Also on top of all of that was the CSS of Modals. Its a HUGE feature that I am super proud of.



## 6. Testing

Everybody's favorite thing.

Using Jest, and building out some basic standard tests took a little while for me. But after building multiple components I got the hang of it.

Been able to write tests that test for images and icons on pages.

Testing if the images or icons would render on the wrong route or URL.

Its not the fun work, but knowing parts of the app I built won't totally fall apart gives me some comfort. 



## 7. Local Db

This has made my productivity while working on the page crawler much faster. Being able to just clear the db table that I was working with, to quickly see changes in my code has been super helpful.

Before I was having to spoof/fail `api` calls, or use `v-if` to spoof the UI.



## 8. Document



Remembering what you built and what you worked on over a specific time is when the real learning happens.

This last month or so at Luro has felt like very fast, but nothing I can't handle.