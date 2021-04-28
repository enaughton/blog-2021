---
layout: layouts/post.njk
title: "Code Challenege: REST API VS GRAPHQL "
date: 2021-04-27T13:30:25.791Z
---
# Project: Build Github's User Search functionality

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

Then after the inital response, you have to make another request to `data.url`
which will return another object of data, with only some of it being useful for this challenge. 

```object
"login": "",
  "id": {int},
  "node_id": "",
  "avatar_url": "",
  "gravatar_id": "",
  "url": "https://api.github.com/users/{username}",
  "html_url": "https://github.com/{username}",
  "followers_url": "https://api.github.com/users/{username}/followers",
  "following_url": "https://api.github.com/users/{username}/following{/other_user}",
  "gists_url": "https://api.github.com/users/{username}/gists{/gist_id}",
  "starred_url": "https://api.github.com/users/{username}/starred{/owner}{/repo}",
  "subscriptions_url": "https://api.github.com/users/{username}/subscriptions",
  "organizations_url": "https://api.github.com/users/{username}/orgs",
  "repos_url": "https://api.github.com/users/{username}/repos",
  "events_url": "https://api.github.com/users/{username}/events{/privacy}",
  "received_events_url": "https://api.github.com/users/{username}/received_events",
  "type": "User",
  "site_admin": false,
  "name": "",
  "company": null,
  "blog": "Blog",
  "location": "",
  "email": null,
  "hireable": null,
  "bio": "",
  "twitter_username": "",
  "public_repos": 29,
  "public_gists": 0,
  "followers": 25,
  "following": 9,
  "created_at": "2017-01-04T01:54:16Z",
  "updated_at": "2021-04-25T14:01:38Z"
```

Two API calls just to get needed data for the challenge. Not to mention that is two API calls just to get one user's data. But it just one way to complete the challenge.


## GraphQL API 

Now this was the first time I had worked with GraphQL other than going through the Gatsby Tutorials for Graphql a couple of years ago. 

I decided to use [Apollo Graphql](https://www.apollographql.com/). 

Very Cool thing about GraphQL 




