## MVC 패턴, 모델1, 모델2

### MVC패턴

MVC 패턴이란 소프트웨어 공학에서 사용되는 소프트웨어 디자인 패턴으로 모델(Model), 뷰(View), 컨트롤러(Controller) 를 구분해서 개발하는 것을 말한다.

정의는 다음과 같다.

**Controller** : 모델에 명령을 보냄으로써 모델의 상태를 변경할 수 있다.

**Model** : 모델의 상태에 변화가 있을 때 컨트롤러와 뷰에 이를 통보한다. 통보를 통해 뷰는 결과를 보여줄 수 있고, 컨트롤러는 모델의 변화에 따른 명령을 추가, 제거, 수정할 수 있다.

**View** : 뷰는 사용자가 볼 결과물을 생성하기 위해 모델로부터 정보를 얻어 온다.

<br>

이를 웹 어플리케이션에 적용해서 쉽게 표현하면 이렇게 표현할 수도 있을듯!

**Model:** 데이터를 가진 객체, 파라미터로 자주 쓰인다. DB의 테이블과 대응하는 경우가 많다.

**View:** UI를 담당한다. 클라이언트 측 기술인 Html, Css, Javascript등으로 만들어진 컨테이너이다.

**Controller:** UI를 통한 사용자의 입력 명령에 응답하고, 및 데이터 흐름 제어를 담당한다.



**MVC 패턴의 최대 장점은 사용자에게 보여지는 프레젠테이션 영역과 비지니스 로직, 데이터 구조가서로 완전히 분리되어 있다는 점이다.**

<br>

### 모델1

모델1은 MVC를 구현하는 방식으로 다음과 같다. ( JSP / Servlet 이 모델1에 해당 )

![20201231_145617](https://user-images.githubusercontent.com/59816811/103732369-8f6bfe80-502a-11eb-81bf-b228d76bdc5e.png)

모델1은 비지니스 로직 영역(Controller)와 프레젠테이션 영역(View)를 같이 구현하는 방식이다. 따라서, 개발 속도가 빠르다는 장점이 있고 단점으로는 Controller와 View가 혼재하므로 유지보수가 어렵다.

<br>

### 모델2

모델2도 마찬가지로 MVC를 구현하는 방식으로 다음과 같다. ( Spring이 모델 2에 해당 )

![20201231_145655](https://user-images.githubusercontent.com/59816811/103732396-998dfd00-502a-11eb-910c-9fd85299d7a5.png)

모델2는 모델1의 단점을 보완하기 위해 비지니스 로직 영역(Controller), 프레젠테이션 영역 (View), 데이터 구조(Model) 을 분리한 방식이다. Controller와 View의 분리로 디자이너와 개발자의 분업이 가능하고 유지보수에 유리하다. 하지만, 개발 설계가 어렵고, 개발 속도가 모델1에 비해 느리다.

<br>

### 마무리

모델1 방식으로 웹 서비스를 개발하는 사례는 거의 없다!

모델2를 익히자!!
