# 2021 소프트웨어공학 3분반

### 1. Teaming and Project selection

> Name / Student Number / Github ID
```
- 강용현 / 20176889 / kyh1116
- 김예슬 / 20185971 / kys97
- 김예령 / 20162049 / kim-yr
- 박민호 / 20176100 / pmhlj73
- 박상우 / 20171670 / psangwoo
- 정가원 / 20184601 / edaisy8864
```

> Project
```
비대면 주문 어플리케이션
```

> Method

> Sub-groups & Mini-projects

### 2. Problem Statement
> The Problem
```
  올해 최저임금은 8720원으로 작년 2020년 대비 1.5%나 인상 되었으며, 최저임금의 인상 폭이 크지 않던 전과는 다르게 최근 5년간 최저임금은  
3000원에 가까운 인상 폭을 보이며 급격히 치솟았다. 코로나19 사태 장기화로 인해 자영업자들의 경제난이 가중되는 상황에서 비싼 최저임금을  
지불하며 아르바이트 생까지 써야 하는 자영업자들의 인건비 부담을 조금이나마 줄이기 위해 우리는 “비대면 주문 어플리케이션”을 구현하려고 한다.  
또한 “비대면 주문 어플리케이션”은 주문을 받는 객체가 사람이기에 발생 할 수 있는 실수들을 줄일 수 있고, 가게가 바쁘고 붐비는 시간대에도 주문이  
꼬이지 않도록 체계적인 주문 시스템을 구축한다. “비대면 주문 어플리케이션”은 기존의 키오스크와 비슷한 방식이지만 테이블마다 패드를 설치하여  
키오스크와 달리 줄을 서서 주문하지 않고 앉은 테이블에서 바로 주문이 가능하다는 장점이 있다.
```
> Scenarios
```
  어플리케이션이 시작될 때 사용자(가게 사장님)는 가게 계정으로 회원가입을 한 후 해당 계정으로 로그인 한다. 가게 계정으로 로그인하면 사용자는  
“Customer”와 “Admin”을 선택하게 된다. 손님이 사용할 어플리케이션에서는 “Customer”를, 사용자(가게 사장님)가 사용할 어플리케이션에서는  
“Admin”을 선택하면 된다. 우선 “Customer”버전을 클릭하면 Table Number를 입력하는 화면이 나오고 Table Number를 입력하면 “Order”, “Login”  
등의 메뉴가 있는 화면이 나타난다. Order 메뉴를 통하여 가게의 음식을 주문할 수 있고, 주문 취소도 가능하다. Login 메뉴를 통하여 로그인과  
간단한 회원가입을 할 수 있다. 주문은 비회원으로도 가능하며 Login을 하면 포인트, 출석도장과 같은 회원만이 누릴 수 있는 부가기능들을 이용할 수  
있다. 손님이 애플리케이션을 통해 주문을 완료하면 해당 주문은 바로 같은 가게 계정의 “Admin”의 화면에 Table Number와 같이 주문목록이  
나타난다. 주문이 들어온 순서대로 화면에 나타나며 각 주문에 대한 대기 시간을 입력할 수 있다. 가게 사장님은 음식이 준비되면 해당 주문을  
"완료"할 수 있고, Admin이 주문을 완료하면 Customer의 화면에 음식이 준비되었다는 알림이 뜬다.
```

### 3. Gathered Requirements

> Requirements (IEEE-830)

#### <Admin 로그인>
```
REQ-1 (FR / 4) : 시스템은 <Admin 로그인> 화면에서 Admin이 마우스의 클릭을 사용하여 “아이디 입력” 텍스트 상자와 “비밀번호 입력” 텍스트 상자를 선택할 수 있게 허용해야 한다.
REQ-2 (FR / 4) : 시스템은 Admin이 키보드를 사용하여 선택된 텍스트 상자에 아이디와 비밀번호를 입력할 수 있게 허용해야 한다.
REQ-3 (FR / 4) : 시스템은 Admin이 마우스의 클릭이나 키보드의 enter키 입력을 사용하여 “로그인” 버튼을 선택할 수 있게 허용해야 한다.
REQ-4 (FR / 3) : 시스템은 Admin이 “로그인” 버튼을 선택했을 때 텍스트 상자에 입력된 아이디와 비밀번호가 데이터베이스 상에 등록되어 있는 데이터와 일치하는지 확인해야 한다.
REQ-5 (FR / 3) : 시스템은 계정 확인에 성공하면 <사용자 모드 선택> 화면으로 이동해야 한다.
REQ-6 (FR / 5) : 시스템은 Admin이 마우스의 클릭을 사용하여 “회원가입” 버튼, “아이디/비밀번호 찾기” 버튼을 선택할 수 있게 허용해야 한다.
REQ-7 (FR / 3) : 시스템은 “회원가입” 버튼이 클릭되면 <Admin 회원가입> 화면으로 이동해야 한다.
REQ-8 (FR / 3) : 시스템은 “아이디/비밀번호 찾기” 버튼이 클릭되면 <Admin 아이디/비밀번호 찾기> 화면으로 이동해야 한다.
REQ-9 (NFR / 5) : 시스템을 실행했을 때 시스템은 “아이디 입력” 텍스트 상자, “비밀번호 입력” 텍스트 상자, “로그인” 버튼, “회원가입” 버튼,  
“아이디/비밀번호 찾기” 버튼을 <Admin 로그인> 화면에 보여주어야 한다.
REQ-10 (NFR / 1) : 시스템은 계정 확인에 실패하면 로그인 실패 메시지 창을 띄워주어야 한다.
```

#### <Admin 회원가입>
```
REQ-11 (FR / 4) : 시스템은 <Admin 회원가입> 화면에서 Admin이 마우스의 클릭을 사용하여 “아이디 입력” 텍스트 상자, “비밀번호 입력” 텍스트 상자,  
“비밀번호 재확인 입력” 텍스트 상자, “이메일 입력” 텍스트 상자를 선택할 수 있게 허용해야 한다.
REQ-12 (FR / 4) : 시스템은 Admin이 키보드를 사용하여 선택된 텍스트 상자에 아이디, 비밀번호, 비밀번호 재확인, 이메일을 입력할 수 있게 허용해야 한다.
REQ-13 (FR / 4) : 시스템은 Admin이 마우스의 클릭을 사용하여 “가입하기” 버튼과 “돌아가기” 버튼을 선택할 수 있게 허용해야 한다.
REQ-14 (FR / 3) : 시스템은 Admin이 “가입하기” 버튼을 선택했을 때 Admin이 입력한 아이디가 아이디 생성조건과 일치하는지 확인해야 한다.
REQ-15 (FR / 3) : 시스템은 Admin이 입력한 아이디가 아이디 생성조건과 일치할 때 Admin이 입력한 아이디가 데이터베이스 상에 등록되어 있는 아이디와 일치하는지 확인해야한다.
REQ-16 (FR / 3) : 시스템은 Admin이 입력한 아이디가 중복되지 않은 새로운 아이디임을 확인하면 Admin이 입력한 비밀번호가 비밀번호 생성조건과 일치하는지 확인해야 한다.
REQ-17 (FR / 3) : 시스템은 Admin이 입력한 비밀번호가 비밀번호 생성조건과 일치함을 확인하면 Admin이 입력한 비밀번호가 Admin이 입력한 비밀번호 재확인과 일치하는지 확인해야한다.
REQ-18 (FR / 3) : 시스템은 Admin이 입력한 비밀번호가 Admin이 입력한 비밀번호 재확인과 일치함을 확인하면 데이터베이스에 새롭게 생성된 계정을 등록해야 한다.
REQ-19 (FR / 3) : 시스템은 Admin이 회원가입 완료 메시지 창이 닫히면 Admin 로그인 화면으로 돌아가야 한다.
REQ-20 (FR / 3) : 시스템은 Admin이 돌아가기 버튼을 선택했을 때 Admin 로그인 화면으로 돌아가야 한다.
REQ-21 (NFR / 5) : 시스템은 <Admin 회원가입> 화면으로 이동했을 때 시스템은 아이디를 입력하는 텍스트 상자, 아이디 생성조건을 보여주는 텍스트, 비밀번호를 입력하는 텍스트 상자,  
비밀번호 생성조건을 보여주는 텍스트, 비밀번호 재확인용 텍스트 상자, 이메일을 입력하는 텍스트 상자, 가입하기 버튼, 돌아가기 버튼을 한 화면에 보여주어야 한다.
REQ-22 (NFR / 1) : 시스템은 Admin이 입력한 아이디가 아이디 생성조건에 불일치함을 확인하면 해당내용을 알리는 경고 메시지 창을 띄워야 한다.
REQ-23 (NFR / 1) : 시스템은 Admin이 입력한 아이디가 이미 존재하는 아이디임을 확인하면 해당내용을 알리는 경고 메시지 창을 띄워야 한다.
REQ-24 (NFR / 1) : 시스템은 Admin이 입력한 비밀번호가 비밀번호 생성조건에 불일치함을 확인하면 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.
REQ-25 (NFR / 1) : 시스템은 Admin이 입력한 비밀번호 재입력이 Admin이 입력한 비밀번호와 불일치함을 확인하면 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.
REQ-26 (NFR / 1) : 시스템은 Admin이 입력한 이메일이 이메일 형식과 불일치함을 확인하면 해당내용을 알리는 경고 메시지 창을 띄워야 한다.
REQ-27 (NFR / 3) : 시스템은 Admin이 입력한 비밀번호가 비밀번호 재확인과 일치함을 확인하면 회원가입 완료 메시지 창을 띄워야 한다.
```


### 4. System Model
