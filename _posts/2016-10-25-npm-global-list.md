---
title: npm global list 보기
---

`npm` 으로 모듈을 설치 할 때는 대개 `global, devDependencies, dependencies` 이렇게 3개로 나눠서 설치를 하게 된다.

`devDependencies, dependencies` 두개는 package.json 에서 항목들을 볼 수 있지만 `global` 로 설치를 하게 되면 어디서 봐야 하는지 막막 할 때가 있다.
(사실 어디서 볼 수 있을지도 모르지만 어디서 보는 모르는건지도...)

그래서 찾아보니 command 에서 볼 수 있는 방법이 있었다.

```powershell
$ npm install -g --depth=0
```
