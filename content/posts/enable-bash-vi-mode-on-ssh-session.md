---
title: How to enable bash's vi mode in SSH sessions
---

Stop typing `set -o vi` every time you log into a SSH server where everyone
uses the `root` user and you can't set `set editing-mode vi` in `~/.inputrc`.
Add this to your ssh config:

```
# ~/.ssh/config
Host duvel
    RequestTTY yes
    RemoteCommand bash -o vi
```
