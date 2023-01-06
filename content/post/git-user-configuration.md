---
title: "Git User Configuration"
date: 2023-01-07T02:29:29+07:00
draft: false
---

Sometimes I need to change the user name and email address for a project or repository. A way to do use the `git config` command. There are three levels of configuration: system, global, and local. My case for global configuration.

```bash
git config --global user.name "Your Name"
git config --global user.email "Email Address"
```

Next, to make sure configuration is correct, you can use:

```bash
git config --list
```

Reference:

* [Git - Configuring User Information](https://git-scm.com/book/en/v2/Getting-Started-First-Time-Git-Setup#_your_identity)
