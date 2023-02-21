---
layout: layouts/post.njk
title: Follow along as I rebuild a text-based course app
date: 2023-02-14T14:47:02.726Z
---

This will be an update to [Emmett's Course App](https://emmetts-course-app.netlify.app/)

The original project was built as my capstone project for Treehouse's full-stack javascript tech degree program. It was built using class-based components in React, a custom-built REST API using Express and Sequelize ORM.



This project is shipped and hosted in a very strange way. The Database uses SQLite3, and I discovered very quickly that there was not a great place to host this. So I went a very different route in my hosting choices. The front end of the course app is hosted on Netlify. The API is hosted on Glitch. The decision to do that was because I found that Glitch would let me host SQLite3 instances.



Follow along while I rebuild this application using Supabase, Prisma, Next.js, and Tailwind CSS.