---
layout: layouts/post.njk
title: "Code Challenege: REST API VS GRAPHQL "
date: 2021-04-27T13:30:25.791Z
---
# The Project: Build Github's User Search functionality

### You can use the REST API or the GraphQL API

I did both! I built out the project using both, and now I am sharing what I have learned about   


First the REST API. 

Pros: Very quick to get the Requests set up, and pretty neat code when using Hooks. 
Cons: Multiple request with a lot of data we don't need. 

The Github API gives minimal data on the first request. Below is the inital 
response.

```object 
0:
avatar_url: "" 
events_url: ""
followers_url: ""
following_url: ""
gists_url: ""
gravatar_id: ""
html_url: ""
id: {int}
login: ""
node_id: ""
organizations_url: ""
received_events_url: "
repos_url: ""
score: 1
site_admin: false
starred_url: ""
subscriptions_url: ""
type: "User"
url: ""
```





