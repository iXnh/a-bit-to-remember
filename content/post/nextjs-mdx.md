---
title: "Nextjs Mdx"
date: 2022-12-06T20:42:42+07:00
draft: false
---

nextjs mdx is syntax for markdown, here i will show you how to add mdx to nextjs project

first, you need to install next-mdx-remote

secondly, you need to create a file named next.config.js
then you need to add this code to next.config.js

```js
module.exports = {
  pageExtensions: ['js', 'jsx', 'mdx'],
}
```

thirdly, you need to create a file named mdx.js
then you need to add this code to mdx.js

```js
import { serialize } from 'next-mdx-remote/serialize'
import { MDXRemote } from 'next-mdx-remote'

export async function getStaticProps() {
  const mdxSource = await serialize('Hello, world!')

  return {
    props: {
      source: mdxSource,
    },
  }
}

export default function Page({ source }) {
  return <MDXRemote {...source} />
}
```

finally, you need to create a file named index.mdx
then you need to add this code to index.mdx

```mdx

# Hello, world!

```

add this code to index.js

```js
import { getStaticProps } from './mdx'

export { getStaticProps }

export { default } from './mdx'
```

and you need to add this code to package.json

```json
{
  "scripts": {
    "dev": "next dev",
    "build": "next build",
    "start": "next start"
  }
}
```

run this command

```bash
npm run dev
```

open this url

```url
http://localhost:3000
```

you will see this

```mdx
# Hello, world!
```

Thats it! Thanks for reading!
