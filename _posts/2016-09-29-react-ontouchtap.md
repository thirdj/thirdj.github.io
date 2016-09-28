---
title: react "Unknown props onTouchTap"
---

react 개발 서버 구축 하던 중에 만난 오류 인데 특이했다.  
지금까지 보지 못 했던, 사실 많은 오류를 만나지도 못 했지만..  

무튼, 해당 오류는 facebook에도 보고 된 오류 인 듯.  

react + material-ui 를 사용 하는 사용자들에게 주로 나타나는 듯 한데 더 찾아 봐야겠다.  

아래는 그 해결 방법.

> npm install material-ui@0.15.2 --save

material-ui 버전을 0.15.2 로 맞춰서 install 해준다.  
install 할 때 버전을 명시하진 않지만 @version 을 적으면 해당 버전을 install 한다.

{% highlight js %}
import injectTapEventPlugin from 'react-tap-event-plugin';

injectTapEventPlugin();
{% endhighlight %}

메인이 되는 js 혹은 jsx 에서 해당 플러그인을 import 하고 함수를 실행 해 준다.
