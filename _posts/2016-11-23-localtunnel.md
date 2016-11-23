---
title: localtunnel
---

며칠전 개발 환경 설정을 하던중 예전부터 필요로 했던 모듈을 찾게 되었다.

무엇인고 하니 `localtunnel`

개발을 할 때는 `localhost` 에서 많이 하게 되는데 만들고 있는 내용을 다른 사람에게 전달 혹은 공유 하고 싶을때가 있다.

그럴경우 `browserSync` 혹은 `git, svn` 에 올린 후 `pull` 받아 설치 후 확인 하세요.  라고 했는데...

모듈은 `로컬 웹서버를 외부에서 접근하게 만들어주는 툴` 이라고 소개를 하고 있다.

> localtunnel exposes your localhost to the world for easy testing and sharing! No need to mess with DNS or deploy just to have others test out your changes.
localtunnel은 쉽게 테스트하고 공유 할 수 있도록 localhost를 전세계에 공개합니다! DNS를 망치거나 다른 사람들이 변경 사항을 테스트하도록 배포 할 필요가 없습니다.

> Great for working with browser testing tools like browserling or external api callback services like twilio which require a public url for callbacks.
browserling 또는 콜백 용 공개 URL이 필요한 twilio와 같은 외부 API 콜백 서비스와 같은 브라우저 테스트 도구로 작업 할 때 유용합니다.

## installation & use

`global` 로 설치가 되어야 한다.

```powershell
$ sudo npm install -g localtunnel
$
$ lt --port 8000
```

현재 진행중인 프로젝트를 실행 시킨후 `lt` 를 실행시켜 주면 `https` 로 웹사이트를 열어준다.

```powershell
$ your url is: https://mxuvhbwrlo.localtunnel.me
```

많이 쓰자.

ps. [localtunnel](https://github.com/localtunnel/localtunnel)
