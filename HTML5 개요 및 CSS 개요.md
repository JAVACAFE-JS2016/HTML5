# 1. HTML5 개요
- HTML5 중요한 특성
  - semantic HTML
    - ex) header, article
  - rich media
    - flash 등 예전에는 안되었지만 vedio element 들이 생김.
- HTML5 참고 사이트
  - HTML5 지원 브라우저 확인 : https://caniuse.com/
  - Modernizr - https://modernizr.com/
  - HTML 스펙  : MDN - https://developer.mozilla.org/ko/Spec
- HTML
  - Markup language
    ```
    - 꺽쇠모양 예)<b></b>
    ```
- Element, Attribute
  ```
  - Element : <div> </div>
  - Attribute : <div id="test"></div> //id가 attribute
  ```
- Element
  - Single tag : 
  ```
  예
  <hr>
  ```
- Attribute
  - Boolean attribute
    - ex) disabled
  - Contenteditablie 속성 : 커서를 올릴때만 수정할 수 있도록 하는 attribute
  - Spellcheck : 오타 입력할 때, 빨간불로 보여줌.
  - tabindex
- <!DOCTYPE HTML> 선언해주는 습관을 가지자. (HTML 대부분 지원하지만, 지원안할 경우도 있으므로..)
- <head>
  - 메타 데이터만 쓰도록
- 부모, 자식, 자손 그리고 형제 -> HTML 내부적으로 Tree 구조로 가지고 있음.
- HTML5 카테고리 확인 : https://www.w3.org/TR/html5/dom.html (파란색 그림)

# 2. CSS  개요
  - @import 의 경우 속도 문제로 안쓰는 것을 권장
  - @charset만 @import앞에 쓸 수 있음.(@import 위에 주석도 쓰면 안됨)
  - 스타일 종류
    - 인라인 스타일
    - 내장 스타일
    - 외부 스타일
    - 사용자 스타일(Safari의 경우 css import하는 설정이 있음)
    - 브라우저 스타일
    - 예외 : !important
    - 인라인 스타일이 적용되어 있는 경우 !important는 우선순위에서 밀림.
  - 동일한 우선 순위 사이에 스타일 순서 결정하기
    - 참고사이트 : http://www.nextree.co.kr/p8468/
      1) 원천 소스 우선 순위
      !important 선언을 한 사용자 스타일 > !important 선언을 한 제작자 스타일 > 제작자 스타일 > 사용자 스타일 > 사용자 도구 선언 (브라우저 자체의 선언)
      2) CSS 명시도(Specificity) 계산법
          !important > id [ 100 ] > class [ 10 ] > tag [ 1 ] > * [ 0 ]
      !important선언을 사용한 형식이 가장 우선 순위가 높습니다. 그래서 다른 선언들을 덮어버릴 수 있기 때문에 꼭 필요한 곳에만 사용해야 합니다.
      이를 제외한 나머지 선택자는 대괄호 "[]"안에 있는 숫자를 각각의 점수로 부여하여 우선순위를 계산합니다.
      - ID 선택자의 갯수를 세어서 개당 100 으로 계산합니다. (= a)
      - 클래스 선택자의 갯수를 세어서 개당 10 으로 계산합니다. (= b)
      - 태그 선택자의 갯수를 세어서 개당 1 로 계산합니다. (= c)
      - 공용 선택자는 모두 0으로 계산합니다. (= d)
      - 가상 엘리먼트는 무시합니다.
      → a + b + c + d의 값이 높은 순서대로 스타일을 적용하는 우선순위를 가지게 됩니다.
  - css 상속
    - 엘리먼트 외형과 관련된 속성들(문자 색이나 폰트의 디테일 등)은 상속되며 페이지의 레이아웃에 관련된 속성들은 상속되지 않는다. 스타일 안에 inherit 값을 넣으면 강제로 브라우저가 해당 속성의 상위 엘리먼트의 밸류값을 상속.
  - 유용한 도구 : selectorgadget.com
