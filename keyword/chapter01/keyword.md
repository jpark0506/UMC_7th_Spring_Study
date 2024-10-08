## 기본키

- 테이블의 각 레코드를 유일하게 식별할 수 있는 필드 혹은 필드의 조합이다.
- 기본키는 속해있는 테이블에서 유일한 값을 가지며, NULL은 불가함

## 왜래키

- 왜래키란, 하나의 테이블에 있는 필드가 다른 테이블의 **기본키**를 참조하여, 두 테이블 간의 관계를 설정하는 역할을 하는 키입니다.

## ER 다이어그램

- ER 다이어그램이란, Entity Relation Diagram의 약자로, 개체와 관계를 중점적으로 표현하는 다이어그램이다.

- **개체**란 단독으로 존재하는 개체를 의미하고, 데이터베이스에서는 테이블을 개체라고 정의한다.

- **속성**이란 개체가 가지고 있는 고유한 속성을 의미한다.

- **관계**란 개체간의 관계를 나타낸다.

## 복합키

- 두 개의 칼럼을 조합해 만든 하나의 고유한 키.

- **주로 하나의 컬럼으로 고유한 키 값을 만들어낼 수 없을 때** 사용한다.

주로 2가지 용도로 사용되는데,

1. 기본키로서의 복합 키

   두 가지 칼럼을 결합해 복합 키를 만들어 기본 키로 사용 가능하다.

2. 왜래키로서의 복합 키

   서로 다른 왜래키나, 원래 있는 칼럼과 왜래키의 조합으로 복합 키를 만들어 사용 가능하다.

## 연관관계

1. 1:1 관계

   두 엔티티 사이에서, 엔티티의 하나의 행이 다른 엔티티의 단 하나의 행과 대응되면, 그 관계는 1:1 관계라고 정의한다.

2. 1:N 관계

   두 엔티티 사이에서, 엔티티의 하나의 행이 다른 엔티티의 여러 행에 대응된다면, 그 관계는 1:N 관계라고 정의한다.

3. N:M 관계

   두 엔티티 사이에서, 여러개의 행이 여러개의 행과 대응된다면, 그 관계는 N:M 관계라고 정의한다.

## 정규화

### 제 1정규형 (1NF)

- 릴레이션에 속한 모든 도메인이 원자값(Atom Value) (에드거 F. 커드)
- 원자값이라는 용어의 모호성 때문에 크리스토퍼 J.데이트는 다른 정의를 내놓았다.
  → 모든 열과 행의 중복 지점에는 (열과 행의) 해당되는 분야에서 **한 개의 값**을 가진다.
  e.g.) A → a (O), A → (a,b,c) (X)

### 제 2정규형 (2NF)

- 키가 아닌 속성들이 기본키에 완전 함수 종속하고, 부분 함수 종속하지 않은 것

### 제 3정규형 (3NF)

- 키가 아닌 모든 속성들이 기본키에 이행적으로 함수 종속되지 않는 릴레이션

### BCNF(3.5 정규형)

- 릴레이션의 결정자가 모두 후보키인 릴레이션

## 반 정규화

### 정규화의 문제점

정규화를 사용하게 되면 조인을 많이 사용하게 됨

→ 조인을 인한 Overhead가 커진다.

### 해결책 → 반정규화(DeNormalization)

데이터의 중복을 허용하고 조인을 줄이는 설계를 하는 반정규화를 사용한다.

### 반정규화 절차

1. 반정규화 대상 조사
2. 다른 유도방법 검토
3. 반정규화 적용

### 반정규화 기법

1. 테이블 반정규화
   - 테이블 병합
   - 테이블 분할
   - 테이블 추가
2. 속성 반정규화
   - 중복 칼럼 추가
   - 파생 칼럼 추가
   - 이력 테이블 칼럼 추가
   - PK에 의한 칼럼 추가
   - 응용시스템 오작동을 위한 칼럼 추가
3. 관계 반정규화
   - 중복 관계 추가

# 추가 과제

## 자바의 접근제어자 4가지

- private: 같은 클래스 내에서만 접근 가능
- protected: 클래스 내부와, 상속받은 클래스나, 같은 패키지에 대해서만 접근 가능
- default: 클래스 내부와 같은 패키지에서 접근 가능
- public: 모든 클래스에 대해서 접근 허용

## 클래스

- 객체를 생성하기 위한 틀로 정의할 수 있다
- 변수와 메서드로 구성되어 있다.
- class 키워드로 선언이 가능하다. new를 통해 클래스의 실체인 인스턴스를 만들 수 있다.

## 상속

- 부모 클래스가 자식 클래스에게 부모의 변수와 메서드를 사용할 수 있게 해주는 것

- 자식 입장에서 부모 클래스는 Super Class, 부모 입장에서 자식 클래스는 Sub Class라고 한다.

- extends 키워드로 상속이 가능하다. 부모는 여러 자식을 상속해줄 수 있지만, 하나의 자식이 여러 부모를 가질 수 없다. 즉, 다중상속이 불가능하다(다이아몬드 문제 때문에)

- 자바의 모든 클래스는, java.lang.Object를 상속 받도록 되어 있다.

## 인터페이스

- 인터페이스는 다른 클래스를 작성할 때 필요한 기본 틀과, 다른 클래스 사이의 매개 변수 역할을 해준다.

- 다중 상속이 불가능한 java 특징 때문에, 인터페이스가 존재한다. 즉, 하나의 클래스는 여러 인터페이스를 상속받을 수 있다.

- 인터페이스는 오직 인터페이스로부터 상속이 가능하다.

- 추상 클래스와는 다르게, 추상 메소드와 상수만 담을 수 있다. 모든 상수는 public static final, 모든 메서드는 public abstract로 선언해야한다.
