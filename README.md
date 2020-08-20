<p align="center">
  <img src="/assets/dot-logo.png" width="150" />
</p>
<p align="center">⭐⭐⭐⭐⭐</p>
<h1 align="center">Dotpict</h1>
<h4 align="center"><a href="https://dotpict.net/"><code>Analyse Dotpict Platform</code></a></h4>
<p align="center">Dotpict is a complete web and mainly mobile platform to share, like, post, create and draw Pixel Arts. And its is a unofficial documentation about the API used by Dotpict.</p>
<p align="center">
  <img  src="https://img.shields.io/badge/type-api_endpoints-purple" alt="Application Category" />
  <img  src="https://img.shields.io/badge/status-working_fine-success" alt="Repo Status" />
  <img  src="https://img.shields.io/badge/where_from-doctpit_web_platform-blue" alt="Repo Ref" />
</p>

<br>

<p align="center">
  <img src="./assets/a.png" width="200">
  <img src="./assets/b.png" width="200">
  <img src="./assets/c.png" width="200">
  <img src="./assets/d.png" width="200">
  <img src="./assets/e.png" width="200">
  <img src="./assets/f.png" width="200">
  <img src="./assets/g.png" width="200">
</p>

<br>

## Considerations

This little documentation was written using only the browser DevTools as a base, so it has limited and incomplete data, but enough to create a good application. If you want to increase and improve the documentation even more, do not hesitate to visit the Dotpict website and/or edit this README.md! Thank you.

## Documentation

- [Setup](#1-setup)
- [Type|Entity definitions](https://github.com/LaksCastro/dotpict-api/blob/master/TYPES.md)
- [Get trending arts](#2-get-trending-arts)
- [Get recent arts](#3-get-recent-arts)
- [Get works of a user](#4-get-works-of-a-user)
- [Get work threads](#5-get-work-threads)
- [Get work data](#6-get-work-data)
- [Search users by name](#7-search-users-by-name)
- [Search works by title](#8-search-works-by-title)
- [Search works by tag](#9-search-works-by-tag)

### 1. Setup

- Base URL: `https://api.dotpicko.net`
- Smart tip on render the Pixel Arts: all image url's will have a small size by default (64x64), so, you may have problems to render it on a normal `<img>` HTML tag. To fix this, continue using the `<img>` tag, but with a additional CSS property:

```css
/* BAD - ALL IMAGES WILL BE SHOW AS LOW QUALITY */
img {
  width: 930px;
  height: 930px;
}

/* GOOD - ALL IMAGES WILL BE RENDERED WITH A GOOD QUALITY USING A PIXEL IMAGE ALGORITHM */
img {
  width: 930px;
  height: 930px;
  image-rendering: pixelated;
}
```

### 2. Get trending arts

- Endpoint: `/works/trend`
- Method: `GET`
- Params:
  - none
- Available query params:
  - `max_id`:
    - description: return a list of works after the work passed on this param
    - usage: use this param to build a pagination system
    - value: any work ID
- Response:

```js
{
  "data": {
    "works": Work[],
    "next_url": string,
    "ranking": {
      "ranking_works": RankedWork[]
    }
  }
}
```

### 3. Get recent arts

- Endpoint: `/v2/works`
- Method: `GET`
- Params:
  - none
- Available query params:
  - `max_id`:
    - description: return a list of works after the work passed on this param
    - usage: use this param to build a pagination system
    - value: any work ID
- Response:

```js
{
  "data": {
    "works": Work[],
    "next_url": string,
    "carousel": {
      "items": CarouselItem[]
    }
  }
}
```

### 4. Get works of a user

- Endpoint: `/users/USER_ID/works`
- Method: `GET`
- Params:
  - `USER_ID`:
    - description: return a list of works of a user with this ID
    - usage: call this endpoint to show details of a user and your contents
    - value: any user ID
- Available query params:
  - `max_id`:
    - description: return a list of works after the work passed on this param
    - usage: use this param to build a pagination system
    - value: any work ID
- Response:

```js
{
  "data": {
    "user": User,
    "works": Work[],
    "next_url": string
  }
}
```

- Note:
  - The field `next_url` can be empty, that means, can be as empty string if the user not have more works

### 5. Get work threads

- Endpoint: `/works/WORK_ID/threads`
- Method: `GET`
- Params:
  - `WORK_ID`:
    - description: return a list of thread of this work ID
    - usage: call this endpoint to get comments/theads of a certain work
    - value: any work ID
- Available query params:
  - `max_id`:
    - description: return a list of works after the work passed on this param
    - usage: use this param to build a pagination system
    - value: any work ID
- Response:

```js
{
  "data": {
    "user": User,
    "works": Work[],
    "next_url": string
  }
}
```

- Note:
  - The field `next_url` can be empty, that means, can be as empty string if the work have no more threads

### 6. Get work data

- Endpoint: `/works/WORK_ID`
- Method: `GET`
- Params:
  - `WORK_ID`:
    - description: return details of a work with this ID
    - usage: call this endpoint to get data/details of a certain work
    - value: any work ID
- Available query params:
  - none
- Response:

```js
{
  "data": {
    "work": Work,
    "user_relationship": UserRelationship
  }
}
```

### 7. Search users by name

- Endpoint: `/users/search_name`
- Method: `GET`
- Params:
  - none
- Available query params:
  - `name`:
    - description: The text that will be used to search a user by name
    - usage: here you put your typed string to search a user by name
    - value: any **encoded** URL String
  - `work_count`:
    - description: The limit of results
    - usage: here you set the results length limit
    - value: any int
  - `max_id`:
    - description: return a list of users after the users passed on this param
    - usage: use this param to build a pagination system
    - value: any user ID
- Response:

```js
{
  "data": {
    "user_summaries": UserSummary[],
    "next_url": string
  }
}
```

- Note:
  - The field `next_url` can be empty, that means, can be as empty string if the search have no more results

### 8. Search works by title

- Endpoint: `/works/search_title`
- Method: `GET`
- Params:
  - none
- Available query params:
  - `title`:
    - description: The text that will be used to search works by title
    - usage: here you put your typed string to search a work by title
    - value: any **encoded** URL String
  - `max_id`:
    - description: return a list of works after the work passed on this param
    - usage: use this param to build a pagination system
    - value: any work ID
- Response:

```js
{
  "data": {
    "works": Work[],
    "next_url": string
  }
}
```

- Note:
  - The field `next_url` can be empty, that means, can be as empty string if the search have no more results
  
### 9. Search works by tag
- Endpoint: `/works/search_tag`
- Method: `GET`
- Params:
  - none
- Available query params:
  - `tag`:
    - description: The text that will be used to search a work with at least one tag that contains this substring
    - usage: here you put your typed string to search a work by tag
    - value: any **encoded** URL String
  - `max_id`:
    - description: return a list of works after the work passed on this param
    - usage: use this param to build a pagination system
    - value: any work ID
- Response:

```js
{
  "data": {
    "works": Work[],
    "next_url": string
  }
}
```

- Note:
  - The field `next_url` can be empty, that means, can be as empty string if the search have no more results
