## 웹 3-Tier-Architecture

![draw1](https://user-images.githubusercontent.com/59816811/103731742-3c457c00-5029-11eb-9005-27cf53786e29.png)

일반적으로 웹은 다음과 같이 3-Tier-Architecture 로 구성한다.

화면에 보여주는 기술을 사용하는 Presentation Tier와

순수한 비지니스 로직을 담고있는 Business Tier,

데이터를 어떤 방식으로 보관하고, 사용하는가에 대한 설계가 들어가는 Persistence Tier 로 나뉜다.

### Presentation Tier

프레젠테이션 계층은 말 그대로 사용자가 직접 마주하게 되는 계층으로 사용자 인터페이스를 지원한다. 쉽게 얘기해 Front-end 라고 얘기할 수 있고 Spring 에서는 JSP, HTML/CSS 를 이용해서 표현한다.



### Business Tier

비지니스 계층은 고객이 원하는 요구사항을 반영하는 계층이다. 요청되는 정보를 처리하고 가공하는 일을 담당하고 쉽게 얘기해 Back-end 라고 얘기할 수 있다. Spring 에서 ~service 로 이름 지어지는 클래스와 해당 메소드들이 Business Tier 를 담당한다.

고객의 요구사항과 정확히 일치하게 설계해야한다.



### Persistence Tier

데이터계층은 데이터베이스와 데이터베이스에 접근하여 데이터를 읽거나 쓰는 것을 처리하는 계층이다. 일반적인 경우에는 쉽게 얘기해 DBMS 라고 얘기할 수 있다.



### 장점

프로젝트를 3-Tier-Architecture 로 구성하는 가장 큰 이유는 "유지보수" 때문이다. 각 영역이 독립적으로 설계되어 나중에 변경이 있더라도 필요한 부분만 교체하면 된다. 또, 업무 분담이 가능해지므로 업무 효율성의 증가도 있다. 

