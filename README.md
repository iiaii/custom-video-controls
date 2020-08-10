# Custom Video Controls

[HTML5 Custom Video Control](https://www.youtube.com/watch?v=V8_wEZD160g)

---
### 아이디어

비디오 태그의 controls 를 해제하고 div, span, input 태그 등에 css와 js로 액션을 입한다.
이벤트의 경우 키보드, 마우스 별로 세부적으로 구분되는 것을 활용하고 비디오 태그의 프로퍼티를 조작하여 구성한다.


---
### video tag

```html
// 일반적인 비디오 태그 사용 예시
<video id="my-video" width="550px" height="320px">
    <source src="https://...">
</video>

// Vue 비디오 태그 사용 예시
<video
:id="content().idx"
:src="content().media"
:poster="content().vodImage"
aspect-ratio="2"
class="black lighten-2 card-video"
width="100%"
volume="1"
:muted="isMuted"
@timeupdate="seekTimeUpdate"
@click="clickVideo"
@mousedown="mouseDownVideo"
@mouseup="mouseUpVideo"
>
</video>
```

- src : 실제 영상의 url이 위치하는 속성으로 src에 명시되는 순간 영상이 일정 부분 로딩된다. (개발자 도구로 확인 가능) 크롬 브라우저의 경우 비디오가 화면에 밖에 있으면 일정 부분 이상으로, 즉끝까지 로딩하지 않고, 화면안에 위치할 때에 영상을 모두 로딩한다.
- muted : boolean 값으로 true면 음소거 false면 소리가 난다.
- controls : boolean 값으로 true면 컨트롤 패널이 나타나고 false면 컨트롤 패널이 없어진다.
- autoplay : boolean 값으로 true면 자동재생 false면 처음에 정지상태이다.


---
[HTML Video DOM Ref](https://www.w3schools.com/tags/ref_av_dom.asp)
