# 프로젝트명

웹 기본 템플릿 -  https://odada-o.github.io/-themplates-html-scss-js/pages/

## 프로젝트 구조

```bash
📂 src/
├── 📂 pages/                       # 페이지 HTML 파일들
│   └── index.html                  # 메인 페이지 HTML 파일
│   └── sub_02.html                  # 서브 페이지 HTML 파일
├── 📂 resources/                   # 리소스 폴더
│   ├── 📂 css/                     # 전역 CSS 파일들
│   ├── 📂 images/                  # images 파일들
│   ├── 📂 js/                      # JavaScript 파일들
│   │   ├── 📂 component/           # 컴포넌트 관련 JS 파일 (특정한 기능을 수행하는 독립적인 UI요소)
│   │   │   └── ui-script.js        # 컴포넌트 스크립트 (버튼, 모달창, 탭 등)
│   │   ├── 📂 pattern/             # 패턴 관련 JS 파일 (반복적이거나 재사용 가능한 기능적 패턴)
│   │   │   └── ui-pattern-script.js # UI 패턴 스크립트 (스크롤 이벤트, 슬라이드 등)
│   ├── 📂 scss/                    # SCSS 파일들
│   │   ├── 📂 component/           # 컴포넌트 관련 SCSS 파일
│   │   │   ├── 📂 mixins/              # 믹스인 파일들
│   │   │   │   ├── _breakpoints.scss    # 브레이크포인트 믹스인
│   │   │   │   ├── _utils.scss         # 유틸리티 믹스인
│   │   │   ├── _include.scss       # 인클루드 스타일
│   │   │   ├── _reset.scss         # 리셋 스타일
│   │   │   └── _variables.scss     # 변수 정의
│   │   ├── 📂 pattern/             # 패턴 관련 SCSS 파일
│   │   │   ├── _p_include.scss     # 인클루드 스타일
│   │   │   ├── _p_common.scss      # 공통 패턴 스타일
│   │   │   ├── _p_content.scss     # 컨텐츠 관련 패턴 스타일
│   │   │   └── _p_layout.scss      # 레이아웃 패턴 스타일
│   │   └── styles.scss             # 전체 스타일 파일
```

## 문자 인코딩(Character Encoding) 설정

문자가 인코딩되는 방식을 설정합니다.

```html
<meta charset="UTF-8" />
```

- `UTF-8`: 초성, 중성, 종성으로 구분하여 문자를 작성(권장)
- `EUC-KR`: 하나의 완성된 글자를 인식

## 뷰포트(Viewport) 렌더링 방식 설정

웹페이지가 화면(Viewport)에 표현되는 방식을 설정합니다.<br>
모바일 환경에서 적용됩니다.

```html
<meta name="viewport" content="width=device-width, initial-scale=1.0" />
```

- `width=device-width`: 화면의 가로 너비를 각 디바이스(Device)의 가로 너비와 동일하게 적용
- `initial-scale=1.0`: 화면의 초기 화면 배율(확대 정도)을 설정
- `user-scalable=no`: 사용자가 디바이스 화면을 확대(`yes`)/축소(`no`)할 수 있는지 설정
- `maximum-scale=1`: 사용자가 화면을 확대할 수 있는 최댓값
- `minimum-scale=1`: 사용자가 화면을 축소할 수 있는 최솟값

## 오픈 그래프(The Open Graph protocol)

웹페이지가 소셜 미디어(페이스북 등)로 공유될 때 우선적으로 활용되는 정보를 지정합니다.

Slack -

<img width="549" alt="image" src="https://github.com/eehd80/-setting/assets/10627436/17b4a0bd-4630-4483-8e82-52c0b4eafdbe">

KakaoTalk -

<img width="246" alt="image" src="https://github.com/eehd80/-setting/assets/10627436/e4eeef46-fe12-410d-bf2e-7037a1b155ae">

[더 많은 오픈 그래프 속성 보기](https://ogp.me/)

```html
<meta property="og:type" content="website" />
<meta property="og:title" content="페이지 제목" />
<meta property="og:description" content="페이지 설명" />
<meta property="og:image" content="http://www.mysite.com/article/article1_featured_image.jpg" />
<meta property="og:url" content="http://www.mysite.com/article/article1.html" />
```

- `og:type`: 페이지의 유형(E.g, `website`, `video.movie`)
- `og:site_name`: 속한 사이트의 이름
- `og:title`: 페이지의 이름(제목)
- `og:description`: 페이지의 간단한 설명
- `og:image`: 페이지의 대표 이미지 주소(URL)
- `og:url`: 페이지 주소(URL)

## 트위터 카드(Twitter Cards)

웹페이지가 소셜 미디어(트위터)로 공유될 때 우선적으로 활용되는 정보를 지정합니다.

[더 많은 트위터 카드 보기](https://developer.twitter.com/en/docs/twitter-for-websites/cards/guides/getting-started)

```html
<meta name="twitter:card" content="summary" />
<meta name="twitter:title" content="페이지 제목" />
<meta name="twitter:description" content="페이지 설명" />
<meta name="twitter:image" content="http://www.mysite.com/article/article1.html" />
<meta name="twitter:domain" content="사이트 명" />
```

- `twitter:card`: 페이지(카드)의 유형(E.g. `summary`, `player`)
- `twitter:site`: 속한 사이트의 이름
- `twitter:title`: 페이지의 이름(제목)
- `twitter:description`: 페이지의 간단한 설명
- `twitter:image`: 페이지의 대표 이미지 주소(URL)
- `twitter:url`: 페이지 주소(URL)

## Favicon(파비콘, favorites icon)

웹페이지를 나타내는 아이콘, 웹페이지의 로고를 설정합니다.<br>
대부분의 경우 루트 경로에 `favicon.ico` 파일을 위치하면 자동으로 로딩하기 때문에 `<link />` 를 작성할 필요가 없습니다.
`favicon.png` 파일을 사용하려면 다음과 같이 `<link />`를 작성하세요.

> 파비콘 이미지는 루트 경로에 있어야 합니다!

```html
<!--<link rel="shortcut icon" href="favicon.ico" />-->
<link rel="icon" href="./favicon.png" />
```

- `favicon.ico` 64 x 64 (px) 또는 32 x 32 또는 16 x 16
- `favicon.png` 500 x 500 (px)

https://www.naver.com/favicon.ico?1

### .ico 파일 제작

이미지를 업로드하면 손쉽게 `.ico` 파일을 제작할 수 있습니다.

[iconifier.net](https://iconifier.net/)

## Naming Case (BEM)

### kebab-case(케밥 표기법)

- kebab-case, header-container, btn-list, menu-list ...
- (하이픈)으로 단어를 연결하는 표기법
- HTML 태그의 class 속성으로 흔히 사용됨

### camelCase(카멜 표기법)

- camelCase, typeName, lightBox, darkBox ...
- 기본적으로 변수명을 모두 소문자로 씀
- 여러 단어가 이어지는 경우 첫 단어를 제외하고 각 단어의 첫글자만 대문자로 지정

### PascalCase(파스칼 표기법)

- PascalCase, TypeName, LightBox, DarkBox ...
- 카멜 표기법과 같으나, 파스칼 표기법은 첫번째 글자도 대문자로 선언

### Snake_case(뱀 표기범)

- snake_case, background_color, light_box, main_container ...
- 단어를 \_(언더바)로 구분하는 표기법

## BEM

https://getbem.com/

BEM이란? CSS 제작 방법론으로, 일종의 네이밍 컨벤션이라고 볼 수 있다. 개발, 디버깅, 유지보수를 위해 가능한 명확하게 네이밍하는 것이 그들의 목표이다.

## Reset.css

각 브라우저의 기본 스타일을 초기화합니다.

```html
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/reset-css@5.0.1/reset.min.css" />1₩ 111
```

## Google Fonts

'pretendard' 폰트의 가변 다이나믹 서브셋를 사용합니다.

https://github.com/orioncactus/pretendard

```html
<link rel="stylesheet" as="style" crossorigin href="https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/variable/pretendardvariable-dynamic-subset.min.css" />
```

```css
@import url("https://cdn.jsdelivr.net/gh/orioncactus/pretendard@v1.3.9/dist/web/variable/pretendardvariable-dynamic-subset.min.css");
```

```css
body {
  font-family: "Pretendard Variable", sans-serif;
}
```

## Google Material Icons

[구글에서 제공하는 머터리얼 아이콘](https://material.io/resources/icons/?style=baseline)을 무료로 사용할 수 있습니다.

[Getting started for web](https://material.io/develop/web/getting-started)

```html
<!-- icons -->
<link href="https://fonts.googleapis.com/css?family=Material+Icons|Material+Icons+Outlined|Material+Icons+Round" rel="stylesheet" />

<!-- symbols -->
<link rel="stylesheet" href="https://fonts.googleapis.com/css2?family=Material+Symbols+Outlined:opsz,wght,FILL,GRAD@NaN,0,0,0" />
```

다음과 같이 사용할 수 있습니다.

```html
<div class="material-icons">upload</div>
```

## font awesome

[사용 빈도가 높은 아이콘](https://fontawesome.com/search)을 유료 버전과 무료 버전이 있습니다.

[Getting started for web](https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css)

```html
<link rel="stylesheet" href="https://cdnjs.cloudflare.com/ajax/libs/font-awesome/6.4.0/css/all.min.css" />
```

다음과 같이 사용할 수 있습니다.

```html
<i class="fa-solid fa-house"></i>
```

## Swiper

[Swiper](https://swiperjs.com/)는 하드웨어 가속 전환과 여러 기본 동작을 갖춘 현대적인 슬라이드 라이브러리입니다.

[Getting Started With Swiper](https://swiperjs.com/get-started)

```html
<!-- in HEAD -->
<link rel="stylesheet" href="https://cdn.jsdelivr.net/npm/swiper@10/swiper-bundle.min.css" />
<script src="https://cdn.jsdelivr.net/npm/swiper@10/swiper-bundle.min.js"></script>

<!-- in BODY -->
<div class="swiper-container">
  <div class="swiper-wrapper">
    <div class="swiper-slide">1</div>
    <div class="swiper-slide">2</div>
    <div class="swiper-slide">3</div>
  </div>
</div>
```

[Swiper API](https://swiperjs.com/swiper-api)(옵션)을 확인하세요!

```js
new Swiper(요소, 옵션);
```

```js
new Swiper(".swiper-container", {
  direction: "vertical", // 수직 슬라이드
  autoplay: true, // 자동 재생 여부
  loop: true, // 반복 재생 여부
});
```

## GSAP & ScrollToPlugin

https://odada.me/333

[GSAP(The GreenSock Animation Platform)](https://greensock.com/gsap/)은 자바스크립트로 제어하는 타임라인 기반의 애니메이션 라이브러리입니다.
[ScrollToPlugin](https://greensock.com/scrolltoplugin/)은 스크롤 애니메이션을 지원하는 GSAP 플러그인입니다.

> 자바스크립트 지식이 뛰어나지 않아도 충분히 사용할 수 있습니다!

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.5.1/gsap.min.js" integrity="sha512-IQLehpLoVS4fNzl7IfH8Iowfm5+RiMGtHykgZJl9AWMgqx0AmJ6cRWcB+GaGVtIsnC4voMfm8f2vwtY+6oPjpQ==" crossorigin="anonymous"></script>
<script src="https://cdnjs.cloudflare.com/ajax/libs/gsap/3.5.1/ScrollToPlugin.min.js" integrity="sha512-nTHzMQK7lwWt8nL4KF6DhwLHluv6dVq/hNnj2PBN0xMl2KaMm1PM02csx57mmToPAodHmPsipoERRNn4pG7f+Q==" crossorigin="anonymous"></script>
```

[.to() 사용법](<https://greensock.com/docs/v3/GSAP/gsap.to()>)
[GSAP Easing](https://greensock.com/docs/v2/Easing)

```js
gsap.to(요소, {
  속성: 값,
  속성: 값,
  duration: 시간,
  ease: "easing", // 애니메이션 속도 조절
  onComplete: function () {
    // 애니메이션이 완료된 후 실행할 콜백 함수
  },
});
```

```js
gsap.to(요소, {
  속성: 값,
  속성: 값,
  duration: 시간,
  scrollTrigger: {
    trigger: 요소, // 기준이 되는 요소
    start: "top center", // 시작 지점 (화면의 어느 지점에서 시작할지)
    end: "bottom center", // 끝 지점 (화면의 어느 지점에서 끝낼지)
    toggleActions: "play none none none", // 액션(재생, 일시정지, 재생, 일시정지)
    scrub: true, // 스크롤에 따라 애니메이션 속도 조절
    markers: true, // 디버깅을 위한 마커 표시
  },
});
```

```js
gsap.to(window, 0.7, {
  scrollTo: 0,
});
```

## AOS

https://odada.me/332

[AOS(Animate On Scroll)](https://michalsnik.github.io/aos/)은 스크롤에 따라 요소를 애니메이션하는 라이브러리입니다.

```html
<link
    rel="stylesheet"
    href="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.css"
    integrity="sha384-+3
    crossorigin="anonymous"
/>
<script
    src="https://cdn.jsdelivr.net/npm/aos@2.3.4/dist/aos.js"
    integrity="sha384-+3
    crossorigin="anonymous"
></script>
```

```js
AOS.init({
  offset: 200, // 시작 지점
  duration: 600, // 애니메이션 지속 시간
  easing: "ease-in-out", // 애니메이션 속도 조절
  delay: 100, // 애니메이션 지연 시간
  once: true, // 한 번만 실행 여부
  anchorPlacement: "top-bottom", // 앵커(요소) 위치
});
```

```html
<div data-aos="fade-up">Fade Up</div>
```

## ScrollMagic

[ScrollMagic](https://github.com/janpaepke/ScrollMagic)은 스크롤과 요소의 상호 작용을 위한 자바스크립트 라이브러리입니다.<br>
대표적으로 어떤 요소가 현재 화면에 보이는 상태인지를 확인할 때 사용합니다.

[ScrollMagic API](http://scrollmagic.io/docs/)

```html
<script src="https://cdnjs.cloudflare.com/ajax/libs/ScrollMagic/2.0.8/ScrollMagic.min.js"></script>
```

```js
new ScrollMagic.Scene({
  // 감시할 장면(Scene)을 추가
  triggerElement: spyEl, // 보여짐 여부를 감시할 요소를 지정
  triggerHook: 0.8, // 화면의 80% 지점에서 보여짐 여부 감시
})
  .setClassToggle(spyEl, "show") // 요소가 화면에 보이면 show 클래스 추가
  .addTo(new ScrollMagic.Controller()); // 컨트롤러에 장면을 할당(필수!)
```

## Youtube API

[IFrame Player API](https://developers.google.com/youtube/iframe_api_reference?hl=ko)를 통해 YouTube 동영상을 제어할 수 있습니다.

유튜브 영상이 출력될 위치에 요소를 지정(생성)합니다.

```html
<!-- in HEAD -->
<script defer src="./js/youtube.js"></script>

<!-- in BODY -->
<div id="player"></div>
```

`onYouTubePlayerAPIReady` 함수 이름은 Youtube IFrame Player API에서 사용하는 이름이기 때문에 다르게 지정하면 동작하지 않습니다!<br>
그리고 함수는 전역(Global) 등록해야 합니다!

[플레이어 매개변수(playerVars)](https://developers.google.com/youtube/player_parameters.html?playerVersion=HTML5&hl=ko#Parameters)에서 더 많은 옵션을 확인할 수 있습니다.

```js
// Youtube IFrame API를 비동기로 로드합니다.
var tag = document.createElement("script");
tag.src = "https://www.youtube.com/iframe_api";
var firstScriptTag = document.getElementsByTagName("script")[0];
firstScriptTag.parentNode.insertBefore(tag, firstScriptTag);

function onYouTubePlayerAPIReady() {
  // <div id="player"></div>
  new YT.Player("player", {
    videoId: "An6LvWQuj_8", // 재생할 유튜브 영상 ID
    playerVars: {
      autoplay: true, // 자동 재생 유무
      loop: true, // 반복 재생 유무
      playlist: "An6LvWQuj_8", // 반복 재생할 유튜브 영상 ID 목록
    },
    events: {
      // 영상이 준비되었을 때,
      onReady: function (event) {
        event.target.mute(); // 음소거!
      },
    },
  });
}
```

# -krds-html-scss-js
# -themplates-html-scss-js
