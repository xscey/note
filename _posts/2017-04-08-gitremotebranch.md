---
layout: post
title: gitで新しいリモートブランチをローカルに持ってくるやり方
date: 2017-04-08
tags: git
---

すぐ忘れるのでメモ。`git pull`ではなく`git branch`を使うところがポイントである。

例えばdevelopブランチを持ってくるときは、

```
git branch develop origin/develop
```

というようにする。

