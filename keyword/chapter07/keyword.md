# RestControllerAdvice

## 정의
- Spring Framework에서 전역 예외 처리를 제공하는 어노테이션.
- 모든 `@RestController`에서 발생하는 예외를 일괄적으로 처리하며, JSON 응답 형식에 최적화.

## `@RestControllerAdvice` 사용 vs 미사용

### 1. 코드 분리와 재사용성
- **사용 시**: 예외 처리 로직이 전용 클래스로 분리되어 재사용 가능.
- **미사용 시**: 각 컨트롤러에 중복 작성 필요, 코드 복잡성 증가. (EX) try catch 문)

---

### 2. 일관된 에러 응답 제공
- **사용 시**: 모든 API에서 동일한 에러 응답 포맷 제공.
- **미사용 시**: 응답 포맷이 컨트롤러마다 달라 클라이언트 처리 어려움.

---

### 3. 유지보수 용이성
- **사용 시**: 중앙 집중화된 예외 처리로 수정 및 관리가 용이.
- **미사용 시**: 예외 처리 로직이 분산되어 수정 작업 번거로움.

---

### 4. 예외 처리 계층 구조
- **사용 시**: 특정 예외와 일반 예외를 계층적으로 처리 가능.
- **미사용 시**: 모든 예외를 동일하게 처리하기 어려움.

---

### 5. 기능 확장성
- **사용 시**: 로깅, 알림 시스템 등과 연계하기 쉬움.
- **미사용 시**: 각 컨트롤러에 로직을 중복 작성해야 함.




# Lombok

## 정의

- 자바 코드에서 반복적인 보일러플레이트 코드를 줄이기 위해 사용하는 라이브러리.
- 어노테이션 기반으로 `getter`, `setter`, `toString`, `equals`, `hashCode` 등의 메서드와 생성자를 자동으로 생성.

## 장점

1. **코드 간결화**
    - `@Getter`, `@Setter`, `@ToString` 등으로 반복적인 메서드 작성 제거.
    - 유지보수성이 높아지고 가독성 향상.
2. **생성자 편의성**
    - `@AllArgsConstructor`, `@NoArgsConstructor`, `@Builder`로 다양한 생성자와 빌더 패턴을 간단히 구현 가능.
3. **생산성 향상**
    - 코드를 줄이고 IDE에서 자동 생성된 코드를 숨길 수 있어 개발 속도 증가.
4. **가독성 개선**
    - 핵심 비즈니스 로직에 집중할 수 있어 클래스 구조가 명확해짐.