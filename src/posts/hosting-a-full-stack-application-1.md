---
layout: layouts/post.njk
title: "Hosting a Full-Stack Application "
date: 2021-03-24T01:25:42.140Z
tags:
  - Technical
---
Most front end projects can be hosted for free online, using something like Github Pages or Netlify, or say a Codepen. Now a full stack application with a database and/or API makes things a little more complicated. 

This project was finished a year ago. Why is it just now getting put out for the world to see? A lot of reasons but the main one is there isn’t a striaght forward solution to get the specific stack hosted. 

The stack is a React front-end, with a REST API with Express using Sequelize ORM to use the SQLite3 database.

The solution I came up with was to host the REST API and database on Glitch.com, and the React front-end on Netlify.