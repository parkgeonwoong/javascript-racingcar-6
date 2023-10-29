## 피드백

- linter와 Code Formatter의 기능을 활용한다. (Prettier, ESLint 도입)
- 커밋 메시지를 의미 있게 작성한다. (기능별로 커밋을 나눈다.)

<br>

## 기능 요구사항

초간단 자동차 경주 게임을 구현한다.

주어진 횟수 동안 n대의 자동차는 전진 또는 멈출 수 있다.

- [ ] 각 자동차에 이름을 부여할 수 있다.

  - [ ] 전진하는 자동차를 출력할 때 자동차 이름을 같이 출력한다.
  - [ ] 자동차 이름은 쉼표(,)를 기준으로 구분하며 이름은 5자 이하만 가능하다.

- [ ] 사용자는 몇 번의 이동을 할 것인지를 입력할 수 있어야 한다.

- [ ] 전진하는 조건은 0에서 9 사이에서 무작위 값을 구한다.

  - [ ] 무작위 값이 4 이상일 경우이다.

- [ ] 자동차 경주 게임을 완료한 후 누가 우승했는지를 알려준다. 우승자는 한 명 이상일 수 있다.

  - [ ] 우승자가 여러 명일 경우 쉼표(,)를 이용하여 구분한다.

- [ ] 사용자가 잘못된 값을 입력한 경우 throw문을 사용해 "[ERROR]"로 시작하는 메시지를 가지는 예외를 발생시킨 후, 애플리케이션은 종료되어야 한다.

<br>

## 기능 요구사항 분석

- 자동차 / 사용자 분리 (객체 or 모델)
- 출력 (뷰)
- 전진 / 멈춤 조건
- 예외처리

<br>

## 입출력 요구사항

- 입력

  - [ ] 경주 할 자동차 이름(이름은 쉼표(,) 기준으로 구분)
  - [ ] 시도할 횟수

- 출력
  - [ ] 각 차수별 실행 결과
  - [ ] 단독 우승자 안내 문구
  - [ ] 공동 우승자 안내 문구

<br>

## 프로그래밍 요구사항

- [x] Node.js 18.17.1 버전에서 실행 가능해야 한다.
  - [x] `nvm install 18.17.1`
  - [x] `nvm use`
- [ ] 프로그램 실행의 시작점은 App.js의 play 메서드이다.

<br>

## 추가된 요구사항

- [x] indent(인덴트, 들여쓰기) depth를 3이 넘지 않도록 구현한다. 2까지만 허용한다.
  - 예를 들어 while문 안에 if문이 있으면 들여쓰기는 2이다.
  - 힌트: indent(인덴트, 들여쓰기) depth를 줄이는 좋은 방법은 함수(또는 메소드)를 분리하면 된다.
- [ ] Jest를 이용하여 본인이 정리한 기능 목록이 정상 동작함을 테스트 코드로 확인한다.
  - 테스트 도구 사용법이 익숙하지 않다면 **tests**/StringTest.js를 참고하여 학습한 후 테스트를 구현한다.