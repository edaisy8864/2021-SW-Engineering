# 2021 소프트웨어공학 3분반

### 1. Teaming and Project selection
```
> Name / Student Number / Github ID
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

올해 최저임금은 8720원으로 작년 2020년 대비 1.5%나 인상 되었으며, 최저임금의 인상 폭이 크지 않던 전과는 다르게 최근 5년간 최저임금은 3000원에 가까운 인상 폭을 보이며 급격히 치솟았다. 코로나19 사태 장기화로 인해 자영업자들의 경제난이 가중되는 상황에서 비싼 최저임금을 지불하며 아르바이트생까지 써야 하는 자영업자들의 인건비 부담을 조금이나마 줄이기 위해 우리는 “비대면 주문 어플리케이션”을 구현하려고 한다. 또한 “비대면 주문 어플리케이션”은 주문을 받는 객체가 사람이기에 발생 할 수 있는 실수들을 줄일 수 있고, 가게가 바쁘고 붐비는 시간대이더라도 주문이 꼬이지 않는 체계적인 주문 시스템을 구축할 수 있다. 
“비대면 주문 어플리케이션”은 기존의 키오스크와 비슷한 방식이지만 테이블마다 패드를 설치하여 키오스크와 달리 줄을 서서 주문하지 않고 앉은 테이블에서 바로 주문이 가능하다는 장점이 있다.
 
> Scenarios

어플리케이션이 시작될 때 사용자(가게 사장님)는 가게 계정으로 회원가입을 한 후 해당 계정으로 로그인 합니다. 가게 계정으로 로그인 하면 사용자는 “Customer”와 “Admin”을 선택하게 됩니다. 손님이 사용할 어플리케이션에서는 “Customer”를 선택하면 되고, 사용자(가게 사장님)가 사용할 어플리케이션에서는 “Admin”을 선택하면 됩니다. 
우선 “Customer”버전을 클릭하면 Table Number를 입력하는 화면이 나오고 Table Number를 입력하면 “Order”, “Login” 등의 메뉴가 있는 화면이 나타납니다. Order메뉴를 통하여 가게의 음식을 주문할 수 있고, 손님은 주문을 취소할 수도 있습니다. Login 메뉴를 통하여 로그인과 간단한 회원가입을 할 수 있습니다. 주문은 비회원으로도 가능하며 Login을 하면 쿠폰과 같은 회원만이 누릴 수 있는 부가기능들을 이용 가능합니다. 
손님이 애플리케이션을 통해 주문을 완료하면 해당 주문은 바로 같은 가게 계정의 “Admin”의 화면에 Table Number와 같이 주문 목록이 나타납니다. 주문이 들어온 순서대로 화면에 나타나며 각 주문에 대한 대기 시간을 입력할 수 있습니다. 가게 사장님은 음식이 준비되면 해당 주문을 완료 할 수 있고, Admin이 주문을 완료하면 Customer의 화면에 음식이 준비되었다는 알림이 뜹니다.


### 3. Gathered Requirements

### 4. System Model
