---
layout: layouts/page.njk
title: Leap Year Mug Club Interest Form
permalink: /leap-year-form/index.html
---

<form action="/submit" method="POST" data-netlify="true">
<p>
    <label for="name">Name:</label>
    <input type="text" id="name" name="name" required>
</p
<p>
    <label for="email">Email:</label>
    <input type="email" id="email" name="email" required>
</P
    <label for="message">Interest:</label>
    <textarea id="message" name="message" required></textarea>
</p>
    <button type="submit">Submit</button>
</form>
