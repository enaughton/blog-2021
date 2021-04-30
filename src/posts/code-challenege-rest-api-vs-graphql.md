---
layout: layouts/post.njk
title: 'Code Challenege: REST API VS GRAPHQL '
date: 2021-04-30T15:03:28.997Z
---

# Project: Build Github's User Search functionality

### You can use the REST API or the GraphQL API

I did both! I built out the project using both, and now I am sharing what I have learned about

First the REST API.

Pros: Very quick to get the Requests set up, and pretty neat code when using Hooks.
Cons: Multiple requests with a lot of data we don't need.

The Github API gives minimal data on the first request. Below is the initial
response.

```
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

After the initial response, you have to make another request to the users `https://api.github.com/users/{username}`
which will return another object of data, with only some of it being useful for this challenge.

```
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

#### What is GraphQL?

[GraphQL is a query language for APIs and a runtime for fulfilling those queries with your existing data. GraphQL provides a complete and understandable description of the data in your API, gives clients the power to ask for exactly what they need and nothing more, makes it easier to evolve APIs over time, and enables powerful developer tools. - GraphQL Site](https://graphql.org/)

Now, this was the first time I had worked with GraphQL other than going through the Gatsby Tutorials for Graphql a couple of years ago.

There are quite a few GraphQL Clients you can use, but I decided to use [Apollo Graphql](https://www.apollographql.com/).

The coolest thing for me is that once you write the query in GraphQL, you get all the data you need for whatever project you are working on, with just ONE API Call!

The GraphQl Query looks like this.

```


const QUERY = gql`
  query SearchUsers($queryString: String!, $count: Int!, $cursor: String) {
    search(query: $queryString, type: USER, first: $count, after: $cursor) {
      userCount
      edges {
        node {
          ... on User {
            id
            login
            avatarUrl
            name
            url
            followers {
              totalCount
            }
            starredRepositories {
              totalCount
            }
          }
        }
      }
      pageInfo {
        hasNextPage
        hasPreviousPage
        endCursor
        startCursor
      }
    }
  }
`;

```

Pretty neat. I will be using GraphQL in the future.
