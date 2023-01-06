---
title: "Material UI Media Query"
date: 2022-12-24T23:14:25+07:00
draft: false
---


what if I want use Material UI for Media Query, here we go!

material-ui provide `useMediaQuery` hook to use media query in react component.
just like any other hook, we need to import it first.

    import { useMediaQuery } from '@mui/material/useMediaQuery';

then

    const isMobile = useMediaQuery('(max-width:600px)');

To change the width of the button when the screen is mobile or not.

```js
import { useMediaQuery } from '@mui/material/useMediaQuery';

const isMobile = useMediaQuery('(max-width:600px)');
const buttonWidth = isMobile ? '100%' : '50%'; // if isMobile is true, button width is 100%, else 50%

<Button variant="contained" color="primary" style={{ width: buttonWidth }}>
  any text
</Button>
```

explain the variable buttonWidth, when isMobile or max-width:600px is true, button width is 100%, else 50%.
