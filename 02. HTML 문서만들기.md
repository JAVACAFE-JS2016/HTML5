# HTML 문서만들기



* 마우스 옆에 글자 따라다니기 간단한 예제

~~~
var div = document.createElement('div');
div.innerHTML = '<h1>FOLLOW<h1>';
document.body.appendChild(div);
document.body.addEventListener('mousemove', (e)=>{
  div.style.left = e.clientX + 'px';
  div.style.top = e.clientY + 'px';
  div.style.position = 'absolute';
})
~~~

* Mordernizr

* 자바스크립트 특성

  * Hosting 작동원리
  * 동적 타입
  * 연산자 기능이 좀 더 있음
  * Undefined 와 null

* HTML 엘리먼트들

  * 참고 사이트 : http://html5ref.clearboth.org/

  * meta 태그에 페에지 새로고침 정의 가능

  * style에 media 속성도 있음

    ~~~
    <style media='print'>
    ~~~

  *  반응형 웹에서 스크린별로 스타일 적용 가능

    ~~~
    <style media='screen AND (max-width:799px}'></style>
    ~~~

  * Favicon 지정가능(브라우저 상단 탭에 이미지 표현)

  * 스크립트의 실행을 미루기

    * async와 defer 속성 사용

  * noscript

    * 자바스크립트가 실행되지 않거나, 자바스크립트를 사용할 수 없는 경우

  * a link에서 #id 없을 경우, name으로 찾아간다.

  * `<br>`은 `<br`>로 쓰는 것이 표준 (`<br/>`도 결과는 똑같이 나오긴 하지만…) - HTML5 스펙확인함

  * `<Li>` 스타일 옵션 다양함

    ~~~
    list-style-type : circle
    ~~~

  * `<li>` value 속성 이용해서 순서 바꿀 수 있다

  * `section` 보다는`article`를 사용하세요.(스펙상) __//TODO :  다음시간에 좀 더 명확하게 개념 알아오는것으로__
