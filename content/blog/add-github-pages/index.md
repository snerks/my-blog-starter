---
title: Deploy to Github Pages
date: "2020-01-05T11:56:03.284Z"
description: "Deploy the blog to Github Pages"
---

## Navigate to the Gatsby Project root folder

`cd C:\[path-to-gatsby-project-folder]\`

## Install gh-pages

`yarn add --dev gh-pages`  
or  
`npm install -D gh-pages`

## gatsby-config.js changes

### Add the Github Repository name to pathPrefix

```javascript
module.exports = {
  pathPrefix: "/my-blog-starter",
}
```

## package.json changes

### Add the Github Repository name to homepage setting

```json
"homepage": "https://snerks.github.io/my-blog-starter",
```

### Add the Github Repository name to repository.url setting

```json
"repository": {
    "type": "git",
    "url": "git+https://github.com/snerks/my-blog-starter.git"
},
```

## scripts changes

### Add a deploy script for gh-pages

```json
"scripts": {
    "deploy": "gatsby build --prefix-paths && gh-pages -d public"
}
```

### Deploy to Github Pages

`yarn run deploy`  
or  
`npm run deploy`

Refer to [this page](https://www.gatsbyjs.org/docs/how-gatsby-works-with-github-pages/), for more details on how to deploy to
[Github Pages](https://www.gatsbyjs.org/docs/how-gatsby-works-with-github-pages/).
