---
title: "Add date format | Hugo"
date: 2022-12-23T21:20:37+07:00
draft: false
---

After my structure post is done, I need to add like date format. In hugo [documentation](https://gohugo.io/functions/dateformat/)  I found time.Format (alias date.Format) like this :

```
{{ time.Format "format" "date" }}
```

For use this function, make sure you have front matter in your post. For example :

```yaml

---
title: "Add date format | Hugo"
date: 2022-12-23T21:20:37+07:00
draft: false
---

```

Then you need to add function. I use `single.html` in `layouts/_default/single.html`

```go
{{ .Date.Format "Monday - Jan 2, 2006" }}
```
