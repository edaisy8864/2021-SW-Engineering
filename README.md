# 2021 소프트웨어공학 3분반

### 1. Teaming and Project selection

#### 1.1 Name / Student Number / Github ID
```
- 강용현 / 20176889 / kyh1116
- 김예슬 / 20185971 / kys97
- 김예령 / 20162049 / kim-yr
- 박민호 / 20176100 / pmhlj73
- 박상우 / 20171670 / psangwoo
- 정가원 / 20184601 / edaisy8864
```

#### 1.2 Project
```
비대면 주문 어플리케이션
```
  
  
### 2. Problem Statement
#### 2.1 The Problem

>  올해 최저임금은 8720원으로 작년 2020년 대비 1.5%나 인상 되었으며, 최저임금의 인상 폭이 크지 않던 전과는 다르게 최근 5년간 최저임금은 3000원에 가까운 인상 폭을 보이며 급격히 치솟았다. 코로나19 사태 장기화로 인해 자영업자들의 경제난이 가중되는 상황에서 비싼 최저임금을 지불하며 아르바이트 생까지 써야 하는 자영업자들의 인건비 부담을 조금이나마 줄이기 위해 우리는 “비대면 주문 어플리케이션”을 구현하려고 한다. 또한 “비대면 주문 어플리케이션”은 주문을 받는 객체가 사람이기에 발생 할 수 있는 실수들을 줄일 수 있고, 가게가 바쁘고 붐비는 시간대에도 주문이 꼬이지 않도록 체계적인 주문 시스템을 구축한다. “비대면 주문 어플리케이션”은 기존의 키오스크와 비슷한 방식이지만 테이블마다 패드를 설치하여 키오스크와 달리 줄을 서서 주문하지 않고 앉은 테이블에서 바로 주문이 가능하다는 장점이 있다.

#### 2.2 Scenarios
>  어플리케이션이 시작될 때 사용자(가게 사장님)는 가게 계정으로 회원가입을 한 후 해당 계정으로 로그인 한다. 가게 계정으로 로그인하면 사용자는 “Customer”와 “Admin”을 선택하게 된다. 손님이 사용할 어플리케이션에서는 “Customer”를, 사용자(가게 사장님)가 사용할 어플리케이션에서는 “Admin”을 선택하면 된다. 우선 “Customer”버전을 클릭하면 Table Number를 입력하는 화면이 나오고 Table Number를 입력하면 “Order”, “Login” 등의 메뉴가 있는 화면이 나타난다. Order 메뉴를 통하여 가게의 음식을 주문할 수 있고, 주문 취소도 가능하다. Login 메뉴를 통하여 로그인과 간단한 회원가입을 할 수 있다. 주문은 비회원으로도 가능하며 Login을 하면 포인트, 출석도장과 같은 회원만이 누릴 수 있는 부가기능들을 이용할 수 있다. 손님이 애플리케이션을 통해 주문을 완료하면 해당 주문은 바로 같은 가게 계정의 “Admin”의 화면에 Table Number와 같이 주문목록이 나타난다. 주문이 들어온 순서대로 화면에 나타나며 각 주문에 대한 대기 시간을 입력할 수 있다. 가게 사장님은 음식이 준비되면 해당 주문을 "완료"할 수 있고, Admin이 주문을 완료하면 Customer의 화면에 음식이 준비되었다는 알림이 뜬다.
  
  
### 3. Gathered Requirements

#### 3.1 Requirements (IEEE-830)

##### <Admin 로그인>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|1|FR|4|시스템은 <Admin 로그인> 화면에서 Admin이 마우스의 클릭을 사용하여 “아이디” 텍스트 상자와 “비밀번호” 텍스트 상자를 선택할 수 있게 허용해야 한다.|
|2|FR|4|시스템은 Admin이 키보드를 사용하여 선택된 텍스트 상자에 아이디와 비밀번호를 입력할 수 있게 허용해야 한다.|
|3|FR|4|시스템은 Admin이 마우스의 클릭이나 키보드의 enter키 입력을 사용하여 “로그인” 버튼을 선택할 수 있게 허용해야 한다.
|4|FR|3|시스템은 Admin이 “로그인” 버튼을 선택했을 때 텍스트 상자에 입력된 아이디와 비밀번호가 데이터베이스 상에 등록되어 있는 데이터와 일치하는지 확인해야 한다.
|5|FR|3|시스템은 계정 확인에 성공하면 <사용자 모드 선택> 화면으로 이동해야 한다.
|6|FR|5|시스템은 Admin이 마우스의 클릭을 사용하여 “회원가입” 버튼, “아이디/비밀번호 찾기” 버튼을 선택할 수 있게 허용해야 한다.
|7|FR|3|시스템은 “회원가입” 버튼이 클릭되면 <Admin 회원가입> 화면으로 이동해야 한다.
|8|FR|3|시스템은 “아이디/비밀번호 찾기” 버튼이 클릭되면 <Admin 아이디/비밀번호 찾기> 화면으로 이동해야 한다.
|9|NFR|5|시스템을 실행했을 때 시스템은 “아이디” 텍스트 상자, “비밀번호” 텍스트 상자, “로그인” 버튼, “회원가입” 버튼, “아이디/비밀번호 찾기” 버튼을 <Admin 로그인> 화면에 보여주어야 한다.|
|10|NFR|1|시스템은 계정 확인에 실패하면 로그인 실패 메시지 창을 띄워주어야 한다.|


##### <Admin 회원가입>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|11|FR|4|시스템은 <Admin 회원가입> 화면에서 Admin이 마우스의 클릭을 사용하여 “아이디” 텍스트 상자, “비밀번호” 텍스트 상자, “비밀번호 재확인” 텍스트 상자, “이메일” 텍스트 상자를 선택할 수 있게 허용해야 한다.|
|12|FR|4|시스템은 Admin이 키보드를 사용하여 선택된 텍스트 상자에 아이디, 비밀번호, 비밀번호 재확인, 이메일을 입력할 수 있게 허용해야 한다.|
|13|FR|4|시스템은 Admin이 마우스의 클릭을 사용하여 “가입하기” 버튼과 “돌아가기” 버튼을 선택할 수 있게 허용해야 한다.|
|14|FR|3|시스템은 Admin이 “가입하기” 버튼을 선택했을 때 텍스트 상자들에 공백이 있는지 확인해야 한다.|
|15|FR|3|시스템은 텍스트 상자에 공백이 없을 때 Admin이 입력한 아이디가 아이디 생성조건과 일치하는지 확인해야 한다.|
|16|FR|3|시스템은 Admin이 입력한 아이디가 아이디 생성조건과 일치할 때 Admin이 입력한 아이디가 데이터베이스 상에 등록되어 있는 아이디와 일치하는지 확인해야한다.|
|17|FR|3|시스템은 Admin이 입력한 아이디가 중복되지 않은 새로운 아이디임을 확인했을 때 Admin이 입력한 비밀번호가 비밀번호 생성조건과 일치하는지 확인해야 한다.|
|18|FR|3|시스템은 Admin이 입력한 비밀번호가 비밀번호 생성조건과 일치함을 확인했을 때 Admin이 입력한 비밀번호가 Admin이 입력한 비밀번호 재확인과 일치하는지 확인해야한다.|
|19|FR|3|시스템은 Admin이 입력한 비밀번호가 Admin이 입력한 비밀번호 재확인과 일치함을 확인했을 때 데이터베이스에 새롭게 생성된 계정을 등록해야 한다.|
|20|FR|3|시스템은 Admin이 회원가입 완료 메시지 창이 닫히면 Admin 로그인 화면으로 돌아가야 한다.|
|21|FR|3|시스템은 Admin이 돌아가기 버튼을 선택했을 때 Admin 로그인 화면으로 돌아가야 한다.|
|22|NFR|5|시스템은 <Admin 회원가입> 화면으로 이동했을 때 "아이디" 텍스트 상자, 아이디 생성조건을 보여주는 텍스트, "비밀번호" 텍스트 상자, 비밀번호 생성조건을 보여주는 텍스트, "비밀번호 재확인" 텍스트 상자, "이메일" 텍스트 상자, "가입하기" 버튼, "돌아가기" 버튼을 화면에 보여주어야 한다.|
|23|NFR|1|시스템은 텍스트 상자에 공백이 있음을 확인하면 해당내용을 알리는 경고 메시지 창을 띄워야 한다.|
|24|NFR|1|시스템은 Admin이 입력한 아이디가 아이디 생성조건에 불일치함을 확인하면 해당내용을 알리는 경고 메시지 창을 띄워야 한다.|
|25|NFR|1|시스템은 Admin이 입력한 아이디가 이미 존재하는 아이디임을 확인하면 해당내용을 알리는 경고 메시지 창을 띄워야 한다.|
|26|NFR|1|시스템은 Admin이 입력한 비밀번호가 비밀번호 생성조건에 불일치함을 확인하면 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|
|27|NFR|1|시스템은 Admin이 입력한 비밀번호 재입력이 Admin이 입력한 비밀번호와 불일치함을 확인하면 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|
|28|NFR|1|시스템은 Admin이 입력한 이메일이 이메일 형식과 불일치함을 확인하면 해당내용을 알리는 경고 메시지 창을 띄워야 한다.|
|29|NFR|3|시스템은 Admin이 입력한 비밀번호가 비밀번호 재확인과 일치함을 확인하면 회원가입 완료 메시지 창을 띄워야 한다.|

##### <Admin 아이디/비밀번호 찾기>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|30|FR|4|시스템은 <Admin 아이디/비밀번호 찾기> 화면에서 Admin이 마우스의 클릭을 사용하여 “등록된 이메일” 텍스트 상자를 선택한 후 키보드를 사용하여 이메일을 입력할 수 있게 허용해야 한다.|
|31|FR|4|시스템은 Admin이 마우스의 클릭을 사용하여 “인증하기” 버튼을 선택할 수 있게 허용해야 한다.|
|32|FR|3|시스템은 Admin이 “인증하기” 버튼을 선택했을 때 텍스트 상자에 입력된 이메일이 데이터베이스 상에 등록되어 있는 데이터와 일치하는지 확인해야 한다.|
|33|FR|3|시스템은 Admin이 입력한 이메일이 데이터베이스 상에 등록되어 있는 데이터와 일치함을 확인하면 무작위 인증번호를 생성하여 데이터베이스에 저장하고 등록된 이메일로 생성된 인증번호를 전송해야 한다.|
|34|FR|3|시스템은 인증번호를 데이터베이스에 저장 한지 3분이 지나면 해당 인증번호를 데이터베이스에서 완전히 삭제시켜야 한다.|
|35|FR|4|시스템은 <Admin 아이디/비밀번호 찾기> 화면에서 Admin이 마우스의 클릭을 사용하여 “인증번호” 텍스트 상자를 선택한 후 키보드를 사용하여 인증번호를 입력할 수 있게 허용해야 한다.|
|36|FR|4|시스템은 Admin이 마우스의 클릭을 사용하여 “인증번호 확인” 버튼을 선택할 수 있게 허용해야 한다.|
|37|FR|4|시스템은 Admin이 “인증번호 확인” 버튼을 선택했을 때 텍스트 상자에 입력된 인증번호가 데이터베이스 상에 저장되어 있는 인증번호와 일치하는지 확인해야 한다.
|38|FR|3|시스템은 "등록된 아이디" 라디오 버튼과 "비밀번호 변경하기" 버튼이 활성화 되었을 때 Admin이 마우스 클릭을 사용하여 이를 선택할 수 있게 허용해야 한다.|
|39|FR|3|시스템은 Admin이 “비밀번호 변경하기” 버튼을 선택했을 때, “등록된 아이디” 라디오 버튼으로 선택된 계정의 <Admin 비밀번호 변경> 화면으로 이동해야 한다.|
|40|FR|3|시스템은 Admin이 마우스의 클릭을 사용하여 “로그인 페이지로” 버튼을 선택할 수 있게 허용해야 한다.|
|41|FR|3|시스템은 Admin이 “로그인 페이지로” 버튼을 선택했을 때 <Admin 로그인> 화면으로 이동해야 한다.|
|42|NFR|5|시스템은 <Admin 아이디/비밀번호 찾기> 화면으로 이동했을 때 "등록된 이메일" 텍스트 상자, “인증하기” 버튼, "인증번호" 텍스트 상자, "인증번호 확인" 버튼, “로그인 페이지로” 버튼을 화면에 보여주어야 한다.|
|43|NFR|1|시스템은 Admin이 입력한 이메일이 데이터베이스 상에 등록되어 있는 데이터에 없으면 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|
|44|NFR|1|시스템은 인증 메일을 전송한 후에 3분의 카운트 다운을 화면에 보여줘야 하며, 3분이 지나면 인증 유효시간이 만료했음을 알려주는 경고 메시지 창을 띄워야 한다.|
|45|NFR|3|시스템은 인증번호의 일치를 확인했을 때 “등록된 아이디” 라디오 버튼과 “비밀번호 변경하기” 버튼을 활성화하여 화면에 보여주어야 한다.|

##### <Admin 비밀번호 변경>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|46|FR|4|시스템은 Admin이 마우스의 클릭을 사용하여 “새로운 비밀번호” 텍스트 상자를 선택한 후 키보드를 사용하여 새로운 비밀번호을 입력할 수 있게 허용해야 한다.|
|47|FR|4|시스템은 Admin이 마우스의 클릭을 사용하여 “비밀번호 재확인” 텍스트 상자를 선택한 후 키보드를 사용하여 비밀번호 재확인을 입력할 수 있게 허용해야 한다.|
|48|FR|4|시스템은 Admin이 마우스의 클릭을 사용하여 “변경하기” 버튼과 “취소” 버튼을 선택할 수 있게 허용해야 한다.|
|49|FR|3|시스템은 Admin이 "변경하기" 버튼을 선택했을 때 Admin이 "새로운 비밀번호" 텍스트 상자에 입력한 새로운 비밀번호가 비밀번호 생성조건과 일치하는지 확인해야 한다.|
|50|FR|3|시스템은 Admin이 입력한 새로운 비밀번호가 비밀번호 생성조건과 일치함을 확인했을 때, Admin이 입력한 새로운 비밀번호가 Admin이 입력한 비밀번호 재확인과 일치하는지 확인해야 한다.|
|51|FR|3|시스템은 Admin이 입력한 새로운 비밀번호가 Admin이 입력한 비밀번호 재확인과 일치함을 확인했을 때, 데이터베이스에 새로운 비밀번호를 저장하고 해당 계정을 로그아웃한 후 <Admin 로그인> 화면으로 이동해야한다.|
|52|FR|3|시스템은 Admin이 "취소" 버튼을 선택했을 때, 해당 계정을 로그아웃한 후 <Admin 로그인> 화면으로 이동해야한다.|
|53|NFR|5|시스템은 <Admin 비밀번호 변경> 화면으로 이동했을 때 "새로운 비밀번호" 텍스트 상자, 비밀번호 생성조건을 보여주는 텍스트, “비밀번호 재확인” 텍스트 상자, "변경하기" 버튼, “취소” 버튼을 화면에 보여주어야 한다.|
|54|NFR|1|시스템은 Admin이 입력한 새로운 비밀번호가 비밀번호 생성조건과 맞지 않으면 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|
|55|NFR|1|시스템은 Admin이 입력한 새로운 비밀번호가 Admin이 입력한 비밀번호 재확인과 일치하지 않으면, 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|
|56|NFR|1|시스템은 Admin이 입력한 새로운 비밀번호가 Admin이 입력한 비밀번호 재확인과 일치함을 확인했을 때, 비밀번호 변경의 성공과 다시 로그인해달라는 알림을 담은 메시지 창을 띄워야한다.|
|57|NFR|1|시스템은 Admin이 "취소" 버튼을 선택했을 때, 보안을 위해 로그아웃 되었음을 알리는 메시지 창을 띄워야한다.|

##### <사용자 모드 선택>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|58|FR|4|시스템은 <사용자 모드 선택> 화면에서 Admin이 마우스의 클릭을 사용하여 “Customer” 버튼과 “Admin” 버튼을 선택할 수 있게 허용해야 한다.|
|59|FR|3|시스템은 Admin이 “Customer” 버튼을 선택했을 때 <Table Number 입력> 화면으로 이동해야 한다.
|60|FR|3|시스템은 Admin이 “Admin” 버튼을 선택했을 때 <Admin 모드> 화면으로 이동해야 한다.
|61|NFR|5|시스템은 <사용자 모드 선택> 화면으로 이동했을 때 "Customer" 버튼과 "Admin" 버튼을 화면에 보여주어야 한다.

##### <Table Number 입력>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|62|FR|4|시스템은 Admin이 마우스의 클릭을 사용하여 “Table Number” 텍스트 상자를 선택한 후 키보드를 사용하여 Table Number를 입력할 수 있게 허용해야 한다.|
|63|FR|4|시스템은 Admin이 마우스의 클릭이나 키보드의 enter키 입력을 사용하여 "확인" 버튼을 선택할 수 있게 허용해야 한다.|
|64|FR|4|시스템은 Admin이 "확인" 버튼을 선택했을 때 Admin이 "Table Number" 텍스트 상자에 입력한 텍스트가 숫자인지 확인해야 한다.|
|65|FR|4|시스템은 입력된 Table Number가 숫자임을 확인했을 때 데이터베이스에 중복되는 Table Number가 있는지 확인해야한다.|
|66|FR|4|시스템은 입력된 Table Number가 데이터베이스에서 중복되지 않음을 확인했을 때 해당 접속 기기의 Mac 주소를 Table Number와 함께 데이터베이스에 등록한 후 <Customer 모드> 화면으로 이동해야 한다.|
|67|NFR|5|시스템은 <Table Number 입력> 화면으로 이동했을 때 "Table Number" 텍스트 상자와 "확인" 버튼을 화면에 보여주어야 한다.|
|68|NFR|1|시스템은 입력된 Table Number가 숫자가 아닌 경우 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|
|69|NFR|1|시스템은 입력된 Table Number가 이미 등록된 번호일 경우 해당 내용을 알리는 메시지 창을 띄워야 한다.|

##### <Customer 모드>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|70|FR|5|시스템은 <Customer 모드> 화면으로 진입 시 애플리케이션이 종료되더라도 Admin 계정 로그인 상태가 유지되게 해야하며, 애플리케이션의 초기 화면은 <Customer 모드>로 유지되어야 한다.|
|71|FR|4|시스템은 <Customer 모드> 화면에서 Admin이 마우스의 클릭을 사용하여 화면 좌측 상단의 “애플리케이션 초기화” 버튼을 선택할 수 있게 허용해야 한다.|
|72|FR|4|시스템은 Admin이 “애플리케이션 초기화” 버튼을 선택한 경우 <애플리케이션 초기화> 화면으로 이동한다.|
|73|FR|4|시스템은 <Customer 모드> 화면에서 Customer가 마우스의 클릭을 사용하여 화면 우측 상단의 “스탬프/포인트” 버튼을 선택할 수 있게 허용해야 한다.|
|74|FR|4|시스템은 Customer가 “스탬프/포인트” 버튼을 선택한 경우 <스탬프/포인트> 화면으로 이동한다.|
|75|FR|4|시스템은 <Customer 모드> 화면에서 Customer가 마우스의 클릭을 사용하여 “Order” 버튼, “Login”(혹은 "Logout". 둘 중 하나의 상태) 버튼을 선택할 수 있게 허용해야 한다.|
|76|FR|4|시스템은 Customer가 "Order" 버튼을 선택했을 때 <주문하기> 화면으로 이동해야 한다.|
|77|FR|4|시스템은 Customer가 "Login" 버튼을 선택했을 때 <Customer 로그인> 화면으로 이동해야 한다.|
|78|FR|4|시스템은 Customer가 "Logout" 버튼을 선택했을 때 Customer 계정이 로그아웃 되며 "Logout" 버튼을 "Login" 버튼으로 변환해야 한다.|
|79|NFR|5|시스템은 <Customer 모드> 화면으로 이동했을 때 "Order" 버튼과 "Login"(혹은 "Logout". 둘 중 하나의 상태) 버튼, “애플리케이션 초기화” 버튼, "스탬프/포인트" 버튼을 화면에 보여주어야 한다.|

![customer 모드](https://user-images.githubusercontent.com/55443383/116080024-84b9a000-a6d3-11eb-9598-ec694fcc5b1a.png)

##### <애플리케이션 초기화>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|80|FR|4|시스템은 Admin이 마우스의 클릭을 사용하여 “비밀번호 확인” 텍스트 상자를 선택한 후 키보드를 사용하여 Admin 계정의 비밀번호을 입력할 수 있게 허용해야 한다.|
|81|FR|4|시스템은 Admin이 마우스의 클릭이나 키보드 enter 키를 사용하여 "확인" 버튼을 선택하면 "비밀번호 확인" 텍스트 상자의 비밀번호가 데이터베이스에 저장된 Admin 계정의 비밀번호와 일치하는지 확인해야한다.|
|82|FR|4|시스템은 Admin이 데이터베이스와 일치하는 비밀번호를 입력한 것을 확인한 경우 해당 기기의 Customer 계정과 Admin 계정을 모두 로그아웃 시키고, 데이터베이스에서 해당 기기의 Table Number와 주문 정보를 초기화하고, <Admin 로그인> 화면으로 돌아가야 한다.|
|83|FR|4|시스템은 Admin이 마우스의 클릭을 사용하여 "돌아가기" 버튼을 선택했을 경우 <Custumer 모드> 화면으로 돌아가야 한다.|
|84|NFR|1|시스템은 "비밀번호 확인" 텍스트 상자와 "확인" 버튼과 "돌아가기" 버튼을 보여주어야 한다.|
|85|NFR|4|시스템은 Customer가 Admin 계정을 임의로 로그아웃 시키거나 Customer 모드 이외의 권한에 접근하지 못하도록 막아야 한다.|

![애플리케이션 초기화](https://user-images.githubusercontent.com/55443383/116079941-6a7fc200-a6d3-11eb-9d59-cd2e535917c5.png)

##### <스탬프/포인트>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|86|FR|4|시스템은 Customer가 비로그인 상태일 경우 <Customer 모드> 화면으로 돌아가도록 해야 한다.|
|87|FR|4|시스템은 Customer가 마우스의 클릭을 사용하여 "뒤로가기" 버튼을 선택할 수 있게 허용해야 한다.|
|88|FR|4|시스템은 Customer가 "뒤로가기" 버튼을 선택했을 때 <Customer 모드> 화면으로 돌아가도록 해야 한다.|
|89|FR|4|시스템은 Customer가 로그인 상태일 경우 해당 Customer 계정의 데이터베이스로부터 스탬프 수와 적립된 포인트에 관한 데이터를 화면에 표시 해야 한다.|
|90|NFR|5|시스템은 <스탬프/포인트> 화면으로 이동했을 때 계정 "스탬프" 그래픽과 , “적립된 포인트" 그래픽, "뒤로가기" 버튼을 화면에 보여주어야 한다.|
|91|NFR|5|시스템은 Customer가 비로그인 상태일 경우 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|

![스탬프포인트](https://user-images.githubusercontent.com/55443383/116079763-2bea0780-a6d3-11eb-99ab-cbc317f14c9b.png)

##### <Customer 로그인>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|91|FR|4|시스템은 <Customer 로그인> 화면에서 Customer가 마우스의 클릭을 사용하여 “아이디” 텍스트 상자와 “비밀번호” 텍스트 상자를 선택하고 키보드를 사용하여 아이디와 비밀번호를 입력할 수 있게 허용해야 한다.
|92|FR|4|시스템은 Customer가 마우스의 클릭이나 키보드의 enter키 입력을 사용하여 “로그인” 버튼을 선택할 수 있게 허용해야 한다.
|93|FR|3|시스템은 Customer가 “로그인” 버튼을 선택했을 때 텍스트 상자에 입력된 아이디와 비밀번호가 데이터베이스 상에 등록되어 있는 데이터와 일치하는지 확인해야 한다.
|94|FR|3|시스템은 Customer 계정 확인에 성공하면 로그인 상태로 <주문하기> 화면으로 이동해야 하며, <Customer 모드>의 "Login" 버튼은 "Logout" 버튼으로 변환되어야 한다.
|95|FR|5|시스템은 Customer가 마우스의 클릭을 사용하여 “회원가입” 버튼, “아이디/비밀번호 찾기” 버튼, "뒤로가기" 버튼을 선택할 수 있게 허용해야 한다.
|96|FR|3|시스템은 “회원가입” 버튼이 클릭되면 <Customer 회원가입> 화면으로 이동해야 한다.
|97|FR|3|시스템은 “아이디/비밀번호 찾기” 버튼이 클릭되면 <Customer 아이디/비밀번호 찾기> 화면으로 이동해야 한다.
|98|FR|3|시스템은 “뒤로가기” 버튼이 클릭되면 <Customer 모드> 화면으로 이동해야 한다.
|99|NFR|5|시스템을 실행했을 때 시스템은 “아이디” 텍스트 상자, “비밀번호” 텍스트 상자, “로그인” 버튼, “회원가입” 버튼, “아이디/비밀번호 찾기” 버튼, "뒤로가기" 버튼을 <Customer 로그인> 화면에 보여주어야 한다.|
|100|NFR|1|시스템은 계정 확인에 실패하면 로그인 실패 메시지 창을 띄워주어야 한다.|

##### <Customer 회원가입>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|101|FR|4|시스템은 <Customer 회원가입> 화면에서 Customer가 마우스의 클릭을 사용하여 “아이디” 텍스트 상자, “비밀번호” 텍스트 상자, “비밀번호 재확인” 텍스트 상자, “이메일” 텍스트 상자를 선택할 수 있게 허용해야 한다.|
|102|FR|4|시스템은 Customer가 키보드를 사용하여 선택된 텍스트 상자에 아이디, 비밀번호, 비밀번호 재확인, 이메일을 입력할 수 있게 허용해야 한다.|
|103|FR|4|시스템은 Customer가 마우스의 클릭을 사용하여 “가입하기” 버튼과 “돌아가기” 버튼을 선택할 수 있게 허용해야 한다.|
|104|FR|3|시스템은 Customer가 “가입하기” 버튼을 선택했을 때 텍스트 상자들에 공백이 있는지 확인해야 한다.|
|105|FR|3|시스템은 텍스트 상자에 공백이 없을 때 Customer가 입력한 아이디가 아이디 생성조건과 일치하는지 확인해야 한다.|
|106|FR|3|시스템은 Customer가 입력한 아이디가 아이디 생성조건과 일치할 때 Customer가 입력한 아이디가 데이터베이스 상에 등록되어 있는 아이디와 일치하는지 확인해야한다.|
|107|FR|3|시스템은 Customer가 입력한 아이디가 중복되지 않은 새로운 아이디임을 확인했을 때 Customer가 입력한 비밀번호가 비밀번호 생성조건과 일치하는지 확인해야 한다.|
|108|FR|3|시스템은 Customer가 입력한 비밀번호가 비밀번호 생성조건과 일치함을 확인했을 때 Customer가 입력한 비밀번호가 Customer가 입력한 비밀번호 재확인과 일치하는지 확인해야한다.|
|109|FR|3|시스템은 Customer가 입력한 비밀번호가 Customer가 입력한 비밀번호 재확인과 일치함을 확인했을 때 데이터베이스에 새롭게 생성된 계정을 등록해야 한다.|
|110|FR|3|시스템은 Customer가 회원가입 완료 메시지 창이 닫히면 Customer 로그인 화면으로 돌아가야 한다.|
|111|FR|3|시스템은 Customer가 돌아가기 버튼을 선택했을 때 Customer 로그인 화면으로 돌아가야 한다.|
|112|NFR|5|시스템은 <Customer 회원가입> 화면으로 이동했을 때 "아이디" 텍스트 상자, 아이디 생성조건을 보여주는 텍스트, "비밀번호" 텍스트 상자, 비밀번호 생성조건을 보여주는 텍스트, "비밀번호 재확인" 텍스트 상자, "이메일" 텍스트 상자, "가입하기" 버튼, "돌아가기" 버튼을 화면에 보여주어야 한다.|
|113|NFR|1|시스템은 텍스트 상자에 공백이 있음을 확인하면 해당내용을 알리는 경고 메시지 창을 띄워야 한다.|
|114|NFR|1|시스템은 Customer가 입력한 아이디가 아이디 생성조건에 불일치함을 확인하면 해당내용을 알리는 경고 메시지 창을 띄워야 한다.|
|115|NFR|1|시스템은 Customer가 입력한 아이디가 이미 존재하는 아이디임을 확인하면 해당내용을 알리는 경고 메시지 창을 띄워야 한다.|
|116|NFR|1|시스템은 Customer가 입력한 비밀번호가 비밀번호 생성조건에 불일치함을 확인하면 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|
|117|NFR|1|시스템은 Customer가 입력한 비밀번호 재입력이 Customer가 입력한 비밀번호와 불일치함을 확인하면 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|
|118|NFR|1|시스템은 Customer가 입력한 이메일이 이메일 형식과 불일치함을 확인하면 해당내용을 알리는 경고 메시지 창을 띄워야 한다.|
|119|NFR|3|시스템은 Customer가 입력한 비밀번호가 비밀번호 재확인과 일치함을 확인하면 회원가입 완료 메시지 창을 띄워야 한다.|

##### <Customer 아이디/비밀번호 찾기>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|120|FR|4|시스템은 <Customer 아이디/비밀번호 찾기> 화면에서 Customer가 마우스의 클릭을 사용하여 “등록된 이메일” 텍스트 상자를 선택한 후 키보드를 사용하여 이메일을 입력할 수 있게 허용해야 한다.|
|121|FR|4|시스템은 Customer가 마우스의 클릭을 사용하여 “인증하기” 버튼을 선택할 수 있게 허용해야 한다.|
|122|FR|3|시스템은 Customer가 “인증하기” 버튼을 선택했을 때 텍스트 상자에 입력된 이메일이 데이터베이스 상에 등록되어 있는 데이터와 일치하는지 확인해야 한다.|
|123|FR|3|시스템은 Customer가 입력한 이메일이 데이터베이스 상에 등록되어 있는 데이터와 일치함을 확인하면 무작위 인증번호를 생성하여 데이터베이스에 저장하고 등록된 이메일로 생성된 인증번호를 전송해야 한다.|
|124|FR|3|시스템은 인증번호를 데이터베이스에 저장 한지 3분이 지나면 해당 인증번호를 데이터베이스에서 완전히 삭제시켜야 한다.|
|125|FR|4|시스템은 <Customer 아이디/비밀번호 찾기> 화면에서 Customer가 마우스의 클릭을 사용하여 “인증번호” 텍스트 상자를 선택한 후 키보드를 사용하여 인증번호를 입력할 수 있게 허용해야 한다.|
|126|FR|4|시스템은 Customer가 마우스의 클릭을 사용하여 “인증번호 확인” 버튼을 선택할 수 있게 허용해야 한다.|
|127|FR|4|시스템은 Customer가 “인증번호 확인” 버튼을 선택했을 때 텍스트 상자에 입력된 인증번호가 데이터베이스 상에 저장되어 있는 인증번호와 일치하는지 확인해야 한다.
|128|FR|3|시스템은 "등록된 아이디" 라디오 버튼과 "비밀번호 변경하기" 버튼이 활성화 되었을 때 Customer가 마우스 클릭을 사용하여 이를 선택할 수 있게 허용해야 한다.|
|129|FR|3|시스템은 Customer가 “비밀번호 변경하기” 버튼을 선택했을 때, “등록된 아이디” 라디오 버튼으로 선택된 계정의 <Customer 비밀번호 변경> 화면으로 이동해야 한다.|
|130|FR|3|시스템은 Customer가 마우스의 클릭을 사용하여 “로그인 페이지로” 버튼을 선택할 수 있게 허용해야 한다.|
|131|FR|3|시스템은 Customer가 “로그인 페이지로” 버튼을 선택했을 때 <Customer 로그인> 화면으로 이동해야 한다.|
|132|NFR|5|시스템은 <Customer 아이디/비밀번호 찾기> 화면으로 이동했을 때 "등록된 이메일" 텍스트 상자, “인증하기” 버튼, "인증번호" 텍스트 상자, "인증번호 확인" 버튼, “로그인 페이지로” 버튼을 화면에 보여주어야 한다.|
|133|NFR|1|시스템은 Customer가 입력한 이메일이 데이터베이스 상에 등록되어 있는 데이터에 없으면 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|
|134|NFR|1|시스템은 인증 메일을 전송한 후에 3분의 카운트 다운을 화면에 보여줘야 하며, 3분이 지나면 인증 유효시간이 만료했음을 알려주는 경고 메시지 창을 띄워야 한다.|
|135|NFR|3|시스템은 인증번호의 일치를 확인했을 때 “등록된 아이디” 라디오 버튼과 “비밀번호 변경하기” 버튼을 활성화하여 화면에 보여주어야 한다.|

##### <Customer 비밀번호 변경>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|136|FR|4|시스템은 Customer가 마우스의 클릭을 사용하여 “새로운 비밀번호” 텍스트 상자를 선택한 후 키보드를 사용하여 새로운 비밀번호을 입력할 수 있게 허용해야 한다.|
|137|FR|4|시스템은 Customer가 마우스의 클릭을 사용하여 “비밀번호 재확인” 텍스트 상자를 선택한 후 키보드를 사용하여 비밀번호 재확인을 입력할 수 있게 허용해야 한다.|
|138|FR|4|시스템은 Customer가 마우스의 클릭을 사용하여 “변경하기” 버튼과 “취소” 버튼을 선택할 수 있게 허용해야 한다.|
|139|FR|3|시스템은 Customer가 "변경하기" 버튼을 선택했을 때 Customer가 "새로운 비밀번호" 텍스트 상자에 입력한 새로운 비밀번호가 비밀번호 생성조건과 일치하는지 확인해야 한다.|
|140|FR|3|시스템은 Customer가 입력한 새로운 비밀번호가 비밀번호 생성조건과 일치함을 확인했을 때, Customer가 입력한 새로운 비밀번호가 Customer가 입력한 비밀번호 재확인과 일치하는지 확인해야 한다.|
|141|FR|3|시스템은 Customer가 입력한 새로운 비밀번호가 Customer가 입력한 비밀번호 재확인과 일치함을 확인했을 때, 데이터베이스에 새로운 비밀번호를 저장하고 해당 계정을 로그아웃한 후 <Customer 로그인> 화면으로 이동해야한다.|
|142|FR|3|시스템은 Customer가 "취소" 버튼을 선택했을 때, 해당 계정을 로그아웃한 후 <Customer가 로그인> 화면으로 이동해야한다.|
|143|NFR|5|시스템은 Customer가 <Customer 비밀번호 변경> 화면으로 이동했을 때 "새로운 비밀번호" 텍스트 상자, 비밀번호 생성조건을 보여주는 텍스트, “비밀번호 재확인” 텍스트 상자, "변경하기" 버튼, “취소” 버튼을 화면에 보여주어야 한다.|
|144|NFR|1|시스템은 Customer가 입력한 새로운 비밀번호가 비밀번호 생성조건과 맞지 않으면 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|
|145|NFR|1|시스템은 Customer가 입력한 새로운 비밀번호가 Customer가 입력한 비밀번호 재확인과 일치하지 않으면, 해당 내용을 알리는 경고 메시지 창을 띄워야 한다.|
|146|NFR|1|시스템은 Customer가 입력한 새로운 비밀번호가 Customer가 입력한 비밀번호 재확인과 일치함을 확인했을 때, 비밀번호 변경의 성공과 다시 로그인해달라는 알림을 담은 메시지 창을 띄워야한다.|
|147|NFR|1|시스템은 Customer가 "취소" 버튼을 선택했을 때, 보안을 위해 로그아웃 되었음을 알리는 메시지 창을 띄워야한다.|

##### <주문하기>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|
|148|FR|4|시스템은 Customer가 최상단 좌측에 "메인으로" 버튼을 마우스의 클릭을 사용하여 선택할 수 있게 허용해야 한다.|
|149|FR|4|시스템은 Custoemr가 "메인으로" 버튼을 선택했을 때 <Customer 모드> 화면으로 되돌아가게 해야한다.
|150|FR|4|시스템은 Customer가 마우스의 클릭을 사용하여 "메인" 탭, "사이드" 탭, "음료 및 디저트" 탭, "서비스" 탭, "공지사항" 탭, "주문완료" 탭을 선택할 수 있게 허용해야 한다.|
|151|FR|4|시스템은 Customer가  "메인" 탭, "사이드" 탭, "음료 및 디저트" 탭, "서비스" 탭에 포함된 다양한 "메뉴" 버튼들을 마우스의 클릭을 사용하여 선택할 수 있게 허용해야 한다.|
|152|FR|4|시스템은 Customer가 "메뉴" 버튼들을 선택했을 때 해당 메뉴가 장바구니 목록에 없을 경우 수량 1의 상태로 장바구니 목록에 추가될 수 있게 허용해야 한다.|
|153|FR|4|시스템은 Customer가 "메뉴" 버튼들을 선택했을 때 해당 메뉴가 장바구니 목록에 있을 경우 해당 항목의 수량이 +1이 되게 허용해야 한다.|
|154|FR|4|시스템은 Customer가 장바구니 목록에서 메뉴의 개수를 조절할 수 있도록 장바구니 목록의 각 항목 우측에 달린 "+"와 "-" 버튼을 마우스의 클릭을 사용하여 선택할 수 있게 허용해야 한다.|
|155|FR|4|시스템은 Customer가 "+" 버튼을 선택한 경우 해당 장바구니 항목의 수량을 +1하고, "-" 버튼을 선택한 경우 해당 장바구니 항목의 수량을 -1해야 한다.|
|156|FR|4|시스템은 장바구니 항목의 수량이 항상 1 이상이 되도록 유지해야 한다.|
|157|FR|4|시스템은 Customer가 장바구니 목록에 담긴 메뉴를 삭제할 수 있도록 장바구니 목록의 각 항목 좌측에 달린 "X" 버튼을 마우스의 클릭을 사용하여 선택할 수 있게 허용해야 한다.|
|158|FR|4|시스템은 Customer가 장바구니 목록에 담긴 메뉴를 주문할 수 있도록 장바구니 목록 우측 하단의 "주문하기" 버튼을 마우스의 클릭을 사용하여 선택할 수 있게 허용해야 한다.|
|159|FR|4|시스템은 "주문하기" 버튼이 선택된 경우 Customer가 선택한 장바구니 항목들을 해당 Table number의 데이터베이스에 저장해야 하며, Admin에게 알림 메시지를 전달하고, Admin의 주문현황을 업데이트 해야한다.|
|160|FR|4|시스템은 Customer가 주문을 취소할 수 있도록 "주문완료" 탭에서 "조리준비중" 상태의 항목에 대한 "주문 취소하기" 버튼을 마우스로 선택할 수 있어야 한다.|
|161|FR|4|시스템은 Customer의 "주문 취소하기" 선택에 대한 확인/취소 메시지 창에서 Customer가 "확인"을 선택했을 때 Admin에게 이를 알리고, Admin의 승인 후 Admin의 주문현황을 업데이트하고, 해당 Table number의 데이터베이스에서 해당 목록을 삭제한 후, "주문완료" 탭에서도 해당 목록을 삭제해야 한다.|
|162|FR|4|시스템은 Customer의 "주문 취소하기" 선택에 대해 Admin이 승인 거부를 할 경우, "주문완료" 탭의 해당 목록을 "조리중" 상태로 변환해야 한다.|
|163|FR|4|시스템은 Customer가 주문을 취소할 수 없도록 "주문완료" 탭에서 항목의 상태가 "조리중" 및 "조리완료" 일 때, "주문 취소하기" 버튼을 비활성화 시켜야 한다.|
|164|FR|4|시스템은 Customer가 로그인한 상태일 때, "주문완료" 탭의 모든 항목이 "조리완료" 상태가 되면 총 주문금액이 "Admin"이 설정한 조건에 만족하는 경우 해당 Customer 계정의 스탬프 개수 혹은 포인트를 적립하여 데이터베이스에 저장하고, 보안을 위해 Customer 계정을 3분 후 자동 로그아웃시켜 <Customer 모드> 화면으로 이동해야 한다.|
|165|NFR|1|시스템은 Customer가 <주문하기> 화면으로 이동했을 때 "메인" 탭, "사이드" 탭, "음료 및 디저트" 탭, "서비스" 탭, "공지사항" 탭, "주문완료" 탭 등 6가지의 탭을 화면 상단에 보여주고, "메인" 탭의 내용을 초기 화면에 디스플레이 한다.|
|166|NFR|1|시스템은 <주문하기> 화면에서 Customer 로그인 상태를 화면 최상단 우측에 항상 보여주어야 한다.|
|167|NFR|4|시스템은 Customer가 "공지사항" 탭에서 가게의 공지사항을 볼 수 있게 허용해야 한다.
|168|NFR|1|시스템은 <주문하기> 화면에서 우측 하단에 장바구니 목록을 리스트형태로 보여주고, 각 리스트의 항목은 좌측부터 "X" 버튼, 메뉴이름, 가격, "-" 버튼, 수량, "+" 버튼을 차례대로 포함하고 있어야 한다.|
|169|NFR|1|시스템은 장바구니 목록 하단 좌측에 장바구니 총 금액을 항상 디스플레이 해야하고, 장바구니 목록 하단 우측에는 "주문하기" 버튼이 표시되어야 한다.|
|170|NFR|4|시스템은 Customer가 주문진행 상황을 실시간으로 알 수 있도록 "주문완료" 탭에서 항목에 대한 조리진행 상황 및 남은 시간을 보여주어야 한다.|
|171|NFR|4|시스템은 Customer가 "주문완료" 탭에서 각 항목의 "주문 취소하기" 버튼을 선택했을 때, 의사를 다시 확인하기 위해 확인/취소 메시지 창을 띄워야 한다.|
|172|NFR|1|시스템은 UI 형태가 직관적이고 쉬워서 누구라도 사용할 수 있어야 한다.|

![주문하기1](https://user-images.githubusercontent.com/55443383/116079458-c8f87080-a6d2-11eb-9cbb-226e7b12782e.png)
![주문하기2](https://user-images.githubusercontent.com/55443383/116079643-065cfe00-a6d3-11eb-8689-26a8a7d54d45.png)

##### <Admin 모드>
|REQ|Type|Priority|Content|
|:---:|:---:|:---:|:---|

### 4. System Model
