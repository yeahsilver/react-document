# 1. 리액트란 무엇인가

## 프론트엔드 라이브러리 / 프레임 워크

> 웹 개발을 하게 될 때, 귀찮은 DOM 관리와 상태값 업데이트 관리를 최소화하고, 오직 기능 개발, 그리고 사용자 인터페이스를 구현하는 것에 집중할 수 있도록 하기 위하여 만들어진 라이브러리 또는 프레임워크. ex) Angular, Ember, Backbone, Vue, React 등



</br>



## 라이브러리 / 프레임워크의 선택

- #### Angular

  - 라우터, HTTP 클라이언트 등 웹 프로젝트에서 필요한 대부분의 도구들이 프레임워크 안에 내장되어있음.
  - 타입스크립트와 함께 사용

- #### React

  - 컴포넌트라는 개념에 집중이 되어있는 라이브러리
  - 데이터를 넣으면 우리가 지정한 유저 인터페이스를 조립하여 보여줌
  - HTTP 클라이언트, 라우터, 심화적 상태 관리 등의 기능들은 내장되어있지 않음
  - 따로 공식 라이브러리가 있는 것이 아니라 개발자가 원하는 스택을 마음대로 골라서 사용할 수 있음

- #### Vue

  - 입문자가 사용하기에 쉬움
  - 단순 CDN에 있는 파일을 로딩하는 형태로 스크립트를 불러와서 사용하기도 편함.
  - HTML을 템플릿처럼 그대로 사용할 수 있음



</br>



## 페이스북은 왜 리액트를 만들게 됐을까?

프레임워크들은 데이터단을 담당하는 Model, 사용자의 화면에서 보여지게 되는 View, 그리고 사용자가 발생시키는 이벤트를 처리해주는 Controller로 이루어져있는 MVC패턴, 그리고 MVVM(View Model), MVW(Whatever) 등의 패턴들로 이루어져있다. 



여기서 공통점은 바로 모델이다. 양방향 바인딩을 통하여 모델에 있는 값이 변하면, 뷰에서도 이를 변환시킨다. 이때 핵심적인 내용은 변화시켜준다는 부분이다. 



변화라는 것은 상당히 복잡한 작업이다. 특정 이벤트가 발생했을 때, 모델에 변화를 일으키고 변화를 일으킴에 따라 어떤 DOM을 가져와서 어떠한 방식으로 뷰를 업데이트 해줄지 로직을 정해야함. 



그래서 페이스북에서는 리액트를 만들기 전

> 그냥 Mutation(변화)를 하지 말자, 그 대신에, 데이터가 바뀌면 그냥 뷰를 날려버리고 새로 만들면 어떨까?



하지만 DOM기반으로 작동하는 페이지는 그때 그때 새로운 뷰를 생성하면 성능적으로 엄청난 문제가 발생한다. 그래서 사용하는 것이 바로 Virtual Dom이다. 



Virtual DOM은 가상의 DOM이다. 변화가 일어나면, 실제로 브라우저의 DOM에 새로운 것을 넣는 것이 아니라, 자바스크립트로 이뤄진 가상 DOM에 한번 렌더링을 하고, 기존의 DOM과 비교를 한 다음 정말 변화가 필요한 곳에만 업데이트 해줌. 



Virtual DOM은 DOM 변화를 최소화시켜주는 역할을 한다. 이 횟수를 최소화 시키는 것은 매우 중요한 이슈이다. 



</br>



## 리액트를 특별하게 만드는 점은?

- ### 생태계

  - 리액트 라이브러리도 정말 만들어진다. JQuery, 혹은 일반 자바스크립트로 만들어진 라이브러리들도 리액트로 Porting되어 많이 작성되고 있다. 더욱이 단순한 기능을 구현하기 위한 라이브러리가 아니라 프로젝트의 구조와 강하게 묶여있는 라우터, 상태 관리 라이브러리들도 매우 다양.

- ### 사용하는 곳이 많다.

  - Airbnb, BBC, Codecademy, Twitch, Wahoo
  - 새로 만들어지는 프로젝트, 또는 리뉴얼되는 프로젝트에 사용



</br>



## 리액트를 사용하게 됨으로써 앞으로 겪게 될 일들

- 리액트는 자유도가 높은 라이브러리이다.
  - 라우터쪽을 보면 React-router, Next.js, After.js 등이 있음.
  - 상태 관리 라이브러리만 해도  Rudex, MobX, fr(e)actal 같은 라이브러리들이 있다. 

- 리액트 컴포넌트 스타일링을 할 때도 한가지 정해진 방식이 있는 것이 아니라 수많은 방식으로 사용할 수 있음. 