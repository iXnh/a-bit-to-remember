---
title: "Nextjs Route Masking"
date: 2022-12-06T20:42:35+07:00
draft: false
---


in this case i will show you how to add route masking to nextjs

first, you need to install next-routes

secondly, you need to create a file named routes.js
then you need to add this code to routes.js
```js
const routes = require('next-routes')()

routes
  .add('blog', '/blog/:slug')

module.exports = routes
```

thirdly, you need to create a file named next.config.js
then you need to add this code to next.config.js
```js

const routes = require('./routes')

```

finally, you need to create a file named index.js
then add this code to index.js
```js
import { Router } from 'next-routes'

const router = Router()

router.pushRoute('blog', { slug: 'hello-world' })
```


