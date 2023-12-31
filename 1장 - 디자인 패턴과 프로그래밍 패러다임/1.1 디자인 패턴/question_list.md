# 문제

1. 디자인 패턴이란 무엇인가?
2. MVC pattern을 간략하게 설명하고, 발생할 수 있는 문제점에 대해 이야기해보세요
3. React의 Virtual DOM은 무엇인가요?
4. CORS는 무엇이고, CORS 에러를 방지하려면 어떻게 해야하나요?
5. 옵저버 패턴을 어떻게 구현하나요?
6. 프록시 서버를 설명하고 사용 사례에 대해 설명해보세요.
7. MVC 패턴을 설명하고 MVVM 패턴과의 차이는 무엇인지 설명해보세요.
8. Singleton 디자인 패턴을 활용하는 경우를 예를 들어 설명해주세요.
   
8-1. 싱글턴 디자인 패턴의 장단점을 설명해주세요.

8-2. 싱글톤 패턴으로 구현된 객체를 인스턴스화하지 않기 위해서는 어떤 방법을 사용해야 할까요?

8-3. 싱글턴 패턴을 사용할 때 발생할 수 있는 동시성 문제는 무엇인가요?

8-4. 싱글턴 객체의 수명 주기는 어떻게 관리되나요? 생성과 소멸 시점은 어떻게 결정되는 건가요?

8-5. 싱글턴 패턴을 사용하는 대신에 의존성 주입(Dependency Injection)을 사용할 수 있는 상황이 있을까요? 어떤 경우에 어느 방식이 더 적합할까요?


## 출처

[[면접을 위한 CS 전공 지식 노트] 01-1 디자인 패턴](https://velog.io/@blcklamb/%EB%A9%B4%EC%A0%91%EC%9D%84-%EC%9C%84%ED%95%9C-CS-%EC%A0%84%EA%B3%B5-%EC%A7%80%EC%8B%9D-%EB%85%B8%ED%8A%B8-01-1-%EB%94%94%EC%9E%90%EC%9D%B8-%ED%8C%A8%ED%84%B4)
[면접스터디 질문 정리](https://hackmd.io/@wkbUFjPxQ2yPCmhAP8Rdog/r1tQMHs8h)

---

### ✏️지혜
1. 디자인 패턴은 프로그램 상에 문제가 발생하였을 때, 상호 관계 등을 이용하여 해결할 수 있도록 하는 ‘규약’이다.
2. MVC 패턴은 모델, 뷰, 컨트롤러로 이루어진 디자인 패턴으로 각각의 구성 요소에만 집중하여 개발할 수 있습니다. 이렇기 때문에 애플리케이션 복잡해질수록 모델과 뷰의 관계가 복잡해지는 단점이 있습니다.
3. d
4. d
5. 옵저버 패턴은 객체의 상태변화를 관찰하다가 상태 변화가 있다면 옵저버들에게 변화를 알려주는 디자인패턴입니다. 이는 자바스크립트에서 프록시 객체를 통해 구현됩니다.
6. 프록시 서버는 서버와 클라이언트 사이에서 클라이언트가 자신으로 통해 다른 네트워크 서비스에 간접적으로 접속할 수 있게 해주는 컴퓨터 시스템입니다. 프록시 서버로 쓰는 CLOUDFLARE는 웹 서버 앞단에 프록시 서버로 두어 DDOS 공격 방어나 HTTPS 구축에 쓰입니다.
7. MVC 패턴은 모델, 뷰, 컨트롤러로 이루어진 디자인 패턴으로 각각의 구성 요소에만 집중하여 개발할 수 있습니다. MVVM은 컨트롤러 대신 뷰를 더 추상화한 계층인 뷰모델을 사용하고 커맨드와 데이터 바인딩을 가지는 것이 특징입니다.
8. 글턴 디자인은 데이터 베이스 연결 모듈에 많이 쓰입니다.

8.1	싱글턴 디자인은 모듈간 결합이 강해 의존성 주입이 필요하다는 단점이 있고, 메모리 낭비를 방지할 수 있고 전역인스턴스로 자원 공유가 쉽다는 장점이 있습니다.

8.2	객체의 생성자를 private으로 설정하여 외부에서 인스턴스화를 막을 수 있습니다
   
8.3	싱글턴 패턴을 사용할 때 동시성 문제는 여러 스레드에서 동시에 접근하여 객체를 수정하거나 상태를 변경할 때 발생할 수 있습니다.

8.4	싱글턴 객체의 수명 주기는 보통 애플리케이션의 라이프사이클과 관련이 있습니다. 객체는 처음 요청될 때 생성되고, 애플리케이션 종료 시 소멸됩니다. 생성과 소멸 시점은 개발자가 제어할 수 있으며, 필요에 따라 지연 초기화나 초기화 과정에서 추가적인 작업을 수 있습니다.

8.5	싱글턴 객체는 모듈간 결합이 강해 의존성 주입이 필요합니다. 의존성 주입은 객체 간의 결합을 느슨하게 만들고 테스트 용이성을 높일 수 있는 방법입니다.


### ✏️ 지수
1.	프로그램을 설계할 때 자주 발생하는 문제들을 해결하기 위한 솔루션이다.
2.	MVC 패턴은 모델, 뷰, 컨트롤러로 이루어진 디자인 패턴이다. MVC 패턴은 어플리케이션이 복잡해지면 모델과 뷰의 관계가 복잡해진다.
3.	R
4.	CORS는 HTTP 헤더 기반 메커니즘이다. 서버가 웹 브라우저에서 리소스를 로드할 때 다른 오리진을 통해 로드하지 못하도록 한다. CORS에러를 방지하기 위해서 프록시 서버를 생성한다.
5.	프록시 객체를 사용하여 구현한다. 프록시 객체를 통해 객체의 속성이나 메소드의 변화 등을 감지하고 이를 미리 설정해 놓은 옵저버들에게 전달한다.
6.	프록시 서버는 클라이언트가 다른 네트워크 서비스에 간접적으로 접속할 수 있도록 해준다. 주로 서버 앞단에서 캐싱, 로깅, 데이터 분석을 서버보다 먼저 한다. 포트 번호 변경을 통해 사용자가 실제 서버의 포트에 접근하지 못하게 할 수 있으며, 공격자의 DDOS 공격을 차단할 수 있다. Nginx를 Node.js 서버 앞단에서 프록시 서버로 이용하여 보안을 강화하기도 한다.
7.	MVC 패턴은 모델, 뷰, 컨트롤러로 이루어진 디자인 패턴이다. 어플리케이션의 구성 요소를 세가지 역할로 구분하여 각각의 구성 요소에만 집중하여 개발할 수 있다. 따라서 재사용성과 확장성이 용이하지만, 어플리케이션이 복잡해질수록 모델과 뷰의 관계가 복잡해진다.
8.	싱글톤 패턴은 특정 용도로 객체를 하나만 생성하여 공용으로 사용하고 싶을 때 활용한다.
   
8-1. 싱글톤 패턴은 생성 비용이 절감된다는 장점이 있다. 이는 하나의 인스턴스만으로 공유하며 사용하기 때문이다. 반면, TDD를 할 때 걸림돌이 된다는 단점이 있다. TDD를 하기 위해서는 각 테스트가 서로 독립적이어야 하는데, 싱글톤 패턴은 각 테스트마다 독립적인 인스턴스를 만들기 어렵기 때문이다.

8-2. 객체의 생성자를 private로 설정하여 외부에서의 인스턴스화를 막을 수 있다.

8-3. 여러 스레드에서 동시에 접근하여 객체를 수정하거나 상태를 변경할 때 발생할 수 있다. 이를 해결하기 위해서는 스레드 안정성을 보장하는 방법을 사용해야 한다.

8-4. 싱글톤 객체의 수명 주기는 보통 어플리케이션의 라이프사이클과 관련이 있다. 객체는 처음 요청될 때 생성되고, 어플리케이션이 종료될 때 소멸된다. 생성과 소멸 시점은 개발자가 제어할 수 있다.

8-5. 싱글톤 객체에 대한 의존성이 생기게 되면 테스트하기 어려워질 수 있다. 따라서, 의존성 주입을 사용하면 객체 간의 결합을 느슨하게 만들고 테스팅을 쉽게할 수 있는 방법이다.

