**Vuejs 라우팅이란**
웹페이지간 이동방법
-> 클라이언트의 요청 경로에 따라 해당하는 컴포넌트를 불러와 페이지를 구성
-> URL 변경 시 변경된 요소 영역만 갱신 (SPA 방식), 유연한 페이지 전환 가능.

**생성 방식**
- 인스턴스 방식으로 생성
    new VueRouter

**렌더링**
- router-view 태그로 선언하면 각 URL에 맞게 컴포넌트들이 매핑된다. 

**라우터 링크**
- 라우팅된 경로로 이동하게끔 앵커 태그 생성
<router-link to="/main">main</router-link>
<!-- convert -->
<a href="#/main" class="">main</a>
