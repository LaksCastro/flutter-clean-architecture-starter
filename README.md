<p align="center">
  <img src="/assets/dot-logo.png" width="150" />
</p>
<p align="center">⭐⭐⭐⭐⭐</p>
<h1 align="center">Dotpict</h1>
<h4 align="center"><a href="https://dotpict.net/"><code>Analyse Dotpict Platform</code></a></h4>
<p align="center">Dotpict is a complete web and mainly mobile platform to share, like, post, create and draw Pixel Arts. And its is a unnoficial documentation about the API used by Dotpict.</p>
<p align="center">
  <img  src="https://img.shields.io/badge/type-api_endpoints-purple" alt="Application Category" />
  <img  src="https://img.shields.io/badge/status-working_fine-success" alt="Repo Status" />
  <img  src="https://img.shields.io/badge/where_from-doctpit_web_platform-blue" alt="Repo Ref" />
</p>

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
