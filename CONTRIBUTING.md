# GitHub 협업 규칙

이 문서는 GitHub 협업 규칙을 담고 있습니다.

## 1. 커밋 컨벤션
커밋 메시지 구조는 header, body, footer 세가지 파트로 나누고, 각 파트는 빈줄을 두어 구분한다.

### Header
머릿말은 아래와 같은 구조로 이루어져 있습니다.
- tag: subject
- tag는 소문자로 시작
- subject는 대문자로 시작

#### Tag
- 태그: 커밋의 종류를 나타냅니다. 주요 태그 아래와 같습니다:

  - `feat`: 새로운 기능 추가
  - `fix`: 버그 수정
  - `docs`: 문서 관련 변경
  - `setting`: 프로젝트 초기 설정
  - `style`: 코드 스타일 변경 (공백, 포맷 등)
  - `refactor`: 코드 리팩토링
  - `test`: 테스트 관련 변경
  - `chore`: 그 외 자잘한 변경

#### Subject
제목은 다음의 규칙을 지킨다.

- 최대 50글자가 넘지 않도록 하고 마침표 및 특수기호는 사용하지 않는다.
- 명령문으로 작성한다.


### Body
본문은 다음의 규칙을 지킨다.

- 본문은 한 줄 당 72자 내로 작성한다.
- 본문 내용은 양에 구애받지 않고 최대한 상세히 작성한다.
- 본문 내용은 어떻게 변경했는지 보다 무엇을 변경했는지 또는 왜 변경했는지를 설명한다.

### Footer
꼬릿말은 다음의 규칙을 지킨다.

- 꼬리말은 optional이고 이슈 트래커 ID를 작성한다.
- 꼬리말은 " #이슈 번호" 형식으로 사용한다.
- 여러 개의 이슈 번호를 적을 때는 쉼표(,)로 구분한다.


### 커밋 메시지 예시
>setting: Add issue template
> (enter)
>To use when implementing new features.
> (enter)
> #1
 
---


## 2. ISSUE / PR
ISSUE / PR은 다음의 규칙을 지킨다.
- ISSUE 기반으로 커밋을 트래킹한다.
- PR은 최소 1명 이상의 확인을 받고 승인해야한다.
- ISSUE / PR은 템플릿을 만들어서 사용하고 아래의 규칙에 따라 제목을 설정해야한다.

### 제목

  - [Feat] 새로운 기능 추가
  - [Fix] 버그 수정
  - [Docs] 문서 관련 변경
  - [Setting] 프로젝트 초기 설정
  - [Style] 코드 스타일 변경 (공백, 포맷 등)
  - [Refactor] 코드 리팩토링
  - [Test] 테스트 관련 변경
  - [Chore] 그 외 자잘한 변경


### ISSUE/PR 제목 예시
> [Feat] Saint+ 모델 구현 
---

## 3. 대회를 위한 Git Flow

### 모델링 가이드

- 새로운 모델을 만들 때, ISSUE를 생성한다. 
     >[FEAT] Saint+ 모델 구현
- master에서 브랜치를 base: 모델명으로 생성한다.
    >base: saint+
- base: 모델명 브랜치에서 사용자명: 모델명으로 브랜치를 생성해서 작업한다.
    >junwon: saint+
- 정상적으로 동작하는 기능이나 공유하고 싶은 자료가 있을 때, base: 모델명 브랜치에 사용자의 branch를 merge한다.

- 모델이 완성되었을 때, master에 base: 모델명을 merge한다.