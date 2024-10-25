# java-racingcar-precourse

# 코드리뷰 개선점

---
- 매직넘버 상수화
- 테스트 클래스 분리
- 의미없는 멤버 변수 삭제
- 변수면 자료형 명시 X
- 메서드명 의미 확실하게
- 어떤 테스트인지 확실하게 명시
- 의미있는 개행

# 기능 요구 사항

--- 
> 초간단 자동차 경주 게임을 구현한다.

- 주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.
- 각 자동차에 이름을 부여할 수 있다. 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
- 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.
- 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.
- 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한 후 무작위 값이 4 이상일 경우이다.
- 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.
- 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.
- 사용자가 잘못된 값을 입력할 경우 IllegalArgumentException을 발생시킨 후 애플리케이션은 종료되어야 한다.


# 입출력 요구 사항 

---

- 입력
  - 경주할 자동차 이름(이름은 쉼표(,) 기준으로 구분)
  - 시도할 횟수
- 출력
  - 차수별 실행 결과
  - 단독 우승자 안내 문구
  - 공동 우승자 안내 문구 

# 설계 

- 자동차
  - [x] 모든 자동차는 위치를 가진다
  - [x] 4 이상일 경우 전진할 수 있다
  - [x] 3 이하일 경우 멈춰있는다
  - [x] 이름은 5자 이하만 가능하다
    - [x] 이름이 5자 초과일 경우 예외
    - [x] 이름이 공백인 경우 예외


- 자동차 경주
  - [ ] 횟수가 주어진다
  - [ ] n대의 자동차가 경주를 한다
  - [ ] 매 차수마다 자동차의 위치를 알아야 한다


- 자동차 공장
  - [ ] 자동차 이름 리스트를 가진다
  - [ ] 자동차 이름으로 자동차 객체 생성


- 랜덤 숫자 생성기
  - [ ] 0에서 9 사이의 무작위 값이 생성된다


- 승자 판별
  - [ ] 자동차 리스트를 가진다
  - [ ] 자동차들의 위치를 비교하여 우승자를 가린다
  - [ ] 우승자는 한 명 이상일 수 있다


- 입력 숫자 검증
  - [ ] 숫자가 아닌 경우 예외
  - [ ] 자연수가 아닌 경우 예외


- 입력
  - [x] 경주할 자동차 이름이 `,`로 구분되어 입력된다
    - [ ] 구분자가 `,`이 아닐경우 예외
  - [x] 시도할 횟수를 입력 받는다


- 출력
  - [x] 차수별로 실행 결과를 출력한다
  - [x] 우승자를 출력한다
    - [x] 단독 우승자인 경우
    - [x] 공동 우승자인 경우


- 테스트
  - [x] 자동차 테스트
    - [x] 4이상일 경우 전진 확인
    - [x] 3이하일 경우 정지 확인
    - [x] 이름이 5자 초과일 경우 예외
    - [x] 이름에 특수문자가 들어갈 경우 예외
  - [ ] 우승자 테스트
    - [ ] 단독 우승자일 경우 확인
    - [ ] 공동 우승자일 경우 확인
  - [ ] 입력 예외 테스트
    - [ ] 구분자가 `,` 가 아닌 경우 예외
    - [ ] 시도할 횟수가 음수일 경우 예외
    - [ ] 시도할 횟수가 숫자가 아닐 경우 예외

# 2024년 10월 25일 15시 55분 1차 개발 시작  
# 2024년 10월 25일 18시 51분 1차 개발 종료(2시간 56분)