## DI (의존성 주입)

### 정의

- 의존성 주입(DI)은 객체의 의존성을 객체 내부에서 직접 생성하는 대신 외부에서 주입받는 디자인 패턴.

### 사용 사례

- Spring과 같은 프레임워크에서 자주 사용되며, 생성자, Setter, 필드 주입를 통해 컴포넌트를 주입받을 수 있음.

### 장점

- 모듈화와 테스트 용이성 향상, 의존성을 쉽게 대체할 수 있음.
- 관심사의 분리를 촉진하여 코드 유지보수가 쉬워짐.

## IoC (제어의 역전)

### 정의

- 제어의 역전(IoC)은 객체 생성과 결합의 제어를 프로그램이 아닌 외부의 컨테이너나 프레임워크가 담당하는 개념.

### 사용 사례

- Spring과 같은 IoC 컨테이너를 사용하는 프레임워크가 애플리케이션 구성요소의 라이프사이클과 설정을 관리함.

### 장점:

- 비즈니스 로직과 객체 생성 로직의 분리로 코드 유지보수가 용이.
- 의존성 관리가 용이하여 테스트와 유지보수성이 향상됨.

## 프레임워크와 API의 차이

### 프레임워크

- 애플리케이션 개발을 위한 구조와 재사용 가능한 코드 집합을 제공하는 도구

### API

- 소프트웨어 컴포넌트 간에 통신할 수 있는 특정 프로토콜과 도구의 집합. 프레임워크와 달리, API는 애플리케이션 구조에 영향을 미치지 않음.

### 차이

- 프레임워크는 애플리케이션의 제어 흐름을 지시하는 반면, API는 특정 기능에 대한 인터페이스를 제공할 뿐이며 프로그램의 구조에는 영향을 주지 않음.

## AOP (관점 지향 프로그래밍)

### 정의

AOP는 교차관심사(cross-cutting concern)를 비즈니스 로직과 분리하는 것을 목표로 하는 프로그래밍 패러다임. 교차관심사는 로깅, 보안, 트랜잭션 관리 등 여러 모듈에서 공통적으로 사용되는 기능을 의미함.

### 주요 개념

- **Aspect**

  - 관심사를 모듈화한 구성 요소
  - 로깅, 보안 같은 공통 기능을 구현하여 코드에 주입

- **Join Point**

  - Aspect가 적용될 수 있는 실행 지점
  - 메서드 호출, 예외 발생, 필드 접근과 같은 이벤트 포함

- **Advice**

  - 실제 수행할 로직을 정의한 부분
  - Before, After, Around와 같이 동작을 제어하는 핵심 역할 수행

- **Pointcut**

  - Aspect를 특정 Join Point에 적용하는 필터 조건
  - 어떤 메서드나 위치에 적용할지 명확하게 설정 가능

- **Weaving**
  - 핵심 로직과 Aspect를 결합하는 과정
  - 컴파일, 클래스 로드, 또는 런타임에 실행 가능
  - AOP 프레임워크가 자동으로 위빙 작업을 처리함

## 서블릿

- 정의: 서블릿은 Java 기반 서버 측 컴포넌트로, HTTP 요청과 응답을 처리. 클라이언트 요청과 서버 자원 간의 중간 계층 역할을 함.
- 사용 사례: 서블릿은 동적 웹 콘텐츠를 생성하는 데 사용되며, 예를 들어 폼 제출 처리, 데이터베이스 데이터를 렌더링할 때 사용됨.
- 장점:
  웹 애플리케이션의 요청 처리가 매우 효율적.
  세션 추적 및 관리가 용이함.
