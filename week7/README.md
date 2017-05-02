# 6조_7주차_회의록

### 팀명
  6조(6월)

### 참가자
  - 정민석 j****** 010 3*** ****
  - 이호용 d****** 010 4*** ****
  - 이수민 l****** 010 5*** ****
  - 구진현 d****** 010 7*** ****

### 일시
  - 2017/04/27 (17:30 ~ 21:30)

### 장소
  1차 제도관 3전산실 / 2차 제도관 1전산실

### 시스템 이름
  screen 배드민턴 시스템(가제 :　알파콕)

### 주제
  screen 야구를 벤치마킹한 screen 배드민턴 시스템을 통해 대국민 스포츠 게임을 제공한다.

### 회의 내용
  1. Class 다이어그램을 각각의 유스케이스에 대해서 만들기로 함 : 먼저 각자 어느정도 유스케이스 부분별로 생각	    을하고 1시간뒤에 합쳐서 진행하기로 하였다. 세부내용은 서로 생각하는 단위나 내용이 다를수있음으로 전반적	   인내용만 생각하고 세부적인 내용은 다같이 결정하기로 하였다. (게임진행의 경우는 너무 복잡해서 다같이 진행)

  2. 회원가입 및 로그인에 대해서 진행
    + '회원가입 UI'의 input, output에 대해서는 서로 의견차이가 많아서 서로 조율함
    + '본인인증처리는' 통신사시스템SI를 추가하여 처리
    + 회원가입정보는 회원정보 중 일부분이라서 나누어서 해야하는데, 어떤 관계로 해야할지 회의함
      - Composition, Generalization으로 할지 고민함
      - 회원가입정보는 회워정보의 일부분이지 하위클래스는 아님으로 Composition으로 진행
    + 로그인의 경우는 전반적인 내용이 다 똑같아서 공통적인 부분만 합쳐서 진행함

  3. 게임 설정 및 게임기록확인에 대해서 진행
    + 게임 설정과 게임기록확인에서는 '개인기록', '게임설정' entity가 생기는데 그것을 회원정보와 어떻게 연결할 지 고민함 : 회원가입정보와는 다르게 개인기록과 게임설정은 비회원의 경우에는 일시적으로 생기고 회원의 경우에는 계속 존재함으로 부분이지만 독릭접으로 존재할수있다고 판단하였다.(Aggregation)
    + 게임 설정과 기록확인에 대한 각각의 UI와 controller를 생성해서 진행함

  4. 게임 진행에 대해서 진행
    + 키오스크와 LCD , 전체 시스템의 애매한 부분에 대해서 고민 : 서로 비슷한 기능이 많아서 개별적으로 나누기 위해서 회의를 통해서 결정
    + 게임진행 관려 여러 DI 들과의 연관관계에 대해서 고민 : 여러 DI 들이 유기적으로 동작하기 때문에 단순한 return 은 제외하고 필요한 함수만 정의

  5. 결제(현금/카드)에 대해서 진행
    + 결제도 현금과 카드 나눠서 카드는 카드사 시스템으로 향하는 컨트롤러 만들어서 보냄
    + 현금은 따로 DI가 없음으로  출력은 함을 boolean 으로 표현함

  6. Entity 클래스에서 각 속성에 대한 getter, setter operation은 생략 : 노트를 통해서 각 속성에대한 함수 생략 표현

  7. 처음에 할때 인터넷이나 다른 요일 분반 조에서 했던 내용이 한 Class 다이어그램에 해놓은걸 보고 그렇게 진행데 조교님게 질문 후 각각 해야하는것을 알게되었다. 그래서 지금까지 해놓것을 각각 하기위해서 나눠서 다시 Usecase별로 Class 다이어그램을 각각 하나씩 따로 만들어 최종본을 완성했다.

### 역할분담
  + 이호용 : Class다이어그램 분석(게임진행 및 게임관련), 총 Class다이어그램 정리
  + 이수민 : Class다이어그램 분석(게임진행 및  회원관련), 총 Class다이어그램 정리
  + 구진현 : Class다이어그램 분석(게임진행 및 게임관련), 회의록 작성
  + 정민석 : Class다이어그램 분석(게임진행 및 회원관련), 회의록 작성
    - **게임관련 :  게임설정, 게임진행, 게임기록확인, 게임설정**
    - **회원관련 : 회원가입, 로그인, 결제, 카드결제, 현금결제**

### 결론 :
  + use case 다이어그램과 분석을 토대로 class 다이어그램을 각각 만듬
  + 생략된 operation을 노트를 통해서 표현
  + 최종본 class 다이어그램과 내용들을 토대로 회의록을 작성