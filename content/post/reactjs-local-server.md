---
title: "Reactjs Local Server"
date: 2023-01-16T07:23:18+07:00
draft: false
---

If you need local server, you can use `json-server` package. It is a fake REST API that you can use to simulate on development project front-end application.

Create new directory.

Route to new directory then Install `json-server` in command prompt/line.

```bash
npm install -g json-server
```

Next, create a file named `db.json` and put in-to root directory of project.
For example:

```json
{
  "data": [
  
        {
            // your any data
        }
  ]
}
```

You can change local server URL by adding `--port` option.

```bash
json-server --watch db.json --port 7000
```

Now, local server running on `http://localhost:7000/data` .
