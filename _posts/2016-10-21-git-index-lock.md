---
title: Unable to create "*/.git/index.lock": File exists.
date: 2016-10-21 18:06:00 +0800
comments: true
permalink: git-index-lock
---

어떤 문제에서 비롯되었는지 모르겠지만 `git pull` 받으려고 하니 `.git/index.lock` 에서 문제가 생겼다고 한다.

여기 저기 찾아 보니 문제는 간단하게 해결이 되었는데.. 이유를 모르겠네...

무튼 해결은

```powershell
$ rm -f ./git/index.lock
```
