# 키친포스

## 요구 사항

### 상품

- 상품을 등록할 수 있다.
- 상품의 가격이 올바르지 않으면 등록할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 이름이 올바르지 않으면 등록할 수 없다.
    - 상품의 이름에는 비속어가 포함될 수 없다.
- 상품의 가격을 변경할 수 있다.
- 상품의 가격이 올바르지 않으면 변경할 수 없다.
    - 상품의 가격은 0원 이상이어야 한다.
- 상품의 가격이 변경될 때 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 크면 메뉴가 숨겨진다.
- 상품의 목록을 조회할 수 있다.

### 메뉴 그룹

- 메뉴 그룹을 등록할 수 있다.
- 메뉴 그룹의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴 그룹의 이름은 비워 둘 수 없다.
- 메뉴 그룹의 목록을 조회할 수 있다.

### 메뉴

- 1 개 이상의 등록된 상품으로 메뉴를 등록할 수 있다.
- 상품이 없으면 등록할 수 없다.
- 메뉴에 속한 상품의 수량은 0 이상이어야 한다.
- 메뉴의 가격이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴는 특정 메뉴 그룹에 속해야 한다.
- 메뉴의 이름이 올바르지 않으면 등록할 수 없다.
    - 메뉴의 이름에는 비속어가 포함될 수 없다.
- 메뉴의 가격을 변경할 수 있다.
- 메뉴의 가격이 올바르지 않으면 변경할 수 없다.
    - 메뉴의 가격은 0원 이상이어야 한다.
- 메뉴에 속한 상품 금액의 합은 메뉴의 가격보다 크거나 같아야 한다.
- 메뉴를 노출할 수 있다.
- 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 메뉴를 노출할 수 없다.
- 메뉴를 숨길 수 있다.
- 메뉴의 목록을 조회할 수 있다.

### 주문 테이블

- 주문 테이블을 등록할 수 있다.
- 주문 테이블의 이름이 올바르지 않으면 등록할 수 없다.
    - 주문 테이블의 이름은 비워 둘 수 없다.
- 빈 테이블을 해지할 수 있다.
- 빈 테이블로 설정할 수 있다.
- 완료되지 않은 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
- 방문한 손님 수를 변경할 수 있다.
- 방문한 손님 수가 올바르지 않으면 변경할 수 없다.
    - 방문한 손님 수는 0 이상이어야 한다.
- 빈 테이블은 방문한 손님 수를 변경할 수 없다.
- 주문 테이블의 목록을 조회할 수 있다.

### 주문

- 1개 이상의 등록된 메뉴로 배달 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 포장 주문을 등록할 수 있다.
- 1개 이상의 등록된 메뉴로 매장 주문을 등록할 수 있다.
- 주문 유형이 올바르지 않으면 등록할 수 없다.
- 메뉴가 없으면 등록할 수 없다.
- 매장 주문은 주문 항목의 수량이 0 미만일 수 있다.
- 매장 주문을 제외한 주문의 경우 주문 항목의 수량은 0 이상이어야 한다.
- 배달 주소가 올바르지 않으면 배달 주문을 등록할 수 없다.
    - 배달 주소는 비워 둘 수 없다.
- 빈 테이블에는 매장 주문을 등록할 수 없다.
- 숨겨진 메뉴는 주문할 수 없다.
- 주문한 메뉴의 가격은 실제 메뉴 가격과 일치해야 한다.
- 주문을 접수한다.
- 접수 대기 중인 주문만 접수할 수 있다.
- 배달 주문을 접수되면 배달 대행사를 호출한다.
- 주문을 서빙한다.
- 접수된 주문만 서빙할 수 있다.
- 주문을 배달한다.
- 배달 주문만 배달할 수 있다.
- 서빙된 주문만 배달할 수 있다.
- 주문을 배달 완료한다.
- 배달 중인 주문만 배달 완료할 수 있다.
- 주문을 완료한다.
- 배달 주문의 경우 배달 완료된 주문만 완료할 수 있다.
- 포장 및 매장 주문의 경우 서빙된 주문만 완료할 수 있다.
- 주문 테이블의 모든 매장 주문이 완료되면 빈 테이블로 설정한다.
- 완료되지 않은 매장 주문이 있는 주문 테이블은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

## 용어 사전
### 메뉴 & 상품

| 한글명             | 영문명             | 설명                                                         |
| ------------------ | ------------------ | ------------------------------------------------------------ |
| 메뉴               | Menu               | 주문 가능한 메뉴                                             |
| 메뉴 그룹          | Menu Group         | 메뉴 분류. 여러 메뉴들을 그룹지어서 담는다.                  |
| 상품               | Product            | 메뉴로 제공되는 상품. 한 상품이 여러 개의 메뉴에 속할 수 있다. |
| 메뉴 상품          | Menu Product       | 메뉴에 속한 상품                                             |
| 수량               | Quantity           | 메뉴에 속한 상품 갯수                                        |
| 메뉴의 상품 총합계액| TotalPriceOfProducts | 메뉴에 속한 상품 금액의 총합                           |
| 비속어             | Profanity          | 이름 설정 시 필터링해야 하는 단어                            |
| 비속어 검증기      | Purgomalum Client  | 문자열에 비속어가 포함되어 있는지 확인해주는 검증기          |

### 메뉴 상태

| 한글명    | 영문명  | 설명                                                         |
| --------- | ------- | ------------------------------------------------------------ |
| 메뉴 노출 | Display | 메뉴가 손님에게 노출되고, 주문이 가능한 상태                 |
| 메뉴 숨김 | Hide    | 가격정보 오류 등의 이유로 손님에게 메뉴를 숨기고, 주문이 불가능한 상태 |

### 주문

| 한글명           | 영문명                | 설명                                                         |
| ---------------- | --------------------- | ------------------------------------------------------------ |
| 주문             | Order                 | 손님이 주문한 내용                                           |
| 주문 항목        | Order Line Item       | 주문을 받은 메뉴를 의미하며 여러 메뉴를 주문 받을 수 있다.   |
| 주문 항목 수량   | quantity              | 주문 받은 항목별 갯수                                          |
| 주문 유형        | Order Type            | 주문 가능한 유형으로 배달, 포장, 매장이 있다.                |
| 주문 상태        | Order Status          | 주문 처리가 어디까지 이루어졌는지 현재의 상태를 의미한다. <br />주문 상태는 포장 및 매장 주문인 경우 '접수 대기 -> 접수 -> 제공 완료 -> 주문 처리 완료'로 진행된다. <br />배달 주문 '접수 대기 -> 접수 -> 제공 완료 -> 배달 중 -> 배달 완료 -> 주문 처리 완료'로 진행된다. |
| 배달 대행사      | Kitchen Riders Client | 배달을 처리해주는 배달 대행사                                |

### 주문 테이블

| 한글명           | 영문명                  | 설명                                                   |
| ---------------- | ----------------------- | ------------------------------------------------------ |
| 주문 테이블      | Order Table             | 손님이 앉는 테이블을 의미하며 주문이 이루어질 수 있다. |
| 주문 테이블 생성 | create                  | 새로운 주문 테이블을 만들고, 빈 테이블로 설정한다.     |
| 손님 수          | Number Of Guests        | 한 테이블에 앉아있는 손님의 인원                       |
| 빈 테이블을 해지 | sit                     | 손님이 테이블에 앉는다.                                |
| 빈 테이블로 설정 | clear                   | 새롭게 주문을 받을 수 있다.                            |

### 주문 유형

| 한글명    | 영문명   | 설명                                                |
| --------- | -------- | --------------------------------------------------- |
| 배달 주문 | DELIVERY | 배달 대행사를 통해 배달 주소로 주문을 배달하는 유형 |
| 포장 주문 | TAKEOUT  | 손님이 매장에서 주문을 찾아가는 유형                |
| 매장 주문 | EAT_IN   | 손님이 매장에서 식사하는 주문 유형                  |

### 주문 상태

| 한글명         | 영문명     | 설명                                                         |
| -------------- | ---------- | ------------------------------------------------------------ |
| 접수 대기      | Waiting    | 손님이 주문한 직후의 상태로 주문이 접수되길 기다리는 상태    |
| 접수           | Accepted   | 대기주문을 매장에서 승인한 상태                              |
| 제공 완료      | Served     | 포장 혹은 매장 내 식사인 경우 상품을 손님에게 제공한 상태,<br />배달인 경우 상품이 준비 완료된 상태 |
| 배달 중        | Delivering | 배달을 출발 상태                                             |
| 배달 완료      | Delivered  | 배달이 완료된 상태                                           |
| 주문 처리 완료 | Completed  | 주문 처리가 완료된 상태                                      |

## 모델링
### 상품(Product) Context
#### 속성
* 식별자(`id`)를 가진다.
* 외부에 노출되는 상품명(`name`)을 가진다.
* 판매 가격(`Price`)를 가진다.

#### 기능/조건
* 상품을 등록한다.
    * 상품은 0원 이상의 가격을 가진다.
        * 상품은 등록하려는 가격이 유효한지 확인한다.
    * 상품명은 비워둘 수 없다.
    * 상품명에 비속어가 포함될 수 없다.
        * 비속어 검증기(`PurgomalumClient`)를 통해 이름에 비속어가 포함되어 있는지 확인한다.
* 상품 가격을 변경한다.
    * 변경하려는 가격은 0원 이상이어야 한다.
        * 상품은 등록하려는 가격이 유효한지 확인한다.
    * 상품 가격 변경 시, `Menu`의 `price`가 `totalPriceOfProducts`보다 커지면 메뉴를 숨긴다.(`hide`)
* 상품 목록을 조회한다.

### 메뉴 그룹(Menu Group) Context
#### 속성
* 식별자(`id`)를 가진다.
* 외부에 노출되는 메뉴그룹명(`name`)을 가진다.

### 기능/조건
* 메뉴 그룹을 등록한다.
    * 메뉴그룹명은 비워둘 수 없다.
    * 메뉴그룹명에 비속어가 포함될 수 없다.
        * 비속어 검증기(`PurgomalumClient`)를 통해 이름에 비속어가 포함되어 있는지 확인한다.
* 메뉴 그룹 목록을 조회한다.

### 메뉴(Menu) Context
#### 속성
* 식별자(`id`)를 가진다.
* 외부에 노출되는 메뉴명(`name`)을 가진다.
* 판매 가격(`price`)을 가진다.
* 메뉴는 자신이 속한 메뉴 그룹(`MenuGroup`)을 가진다.
    * 메뉴는 자신이 속한 메뉴 그룹을 식별하기 위한 `MenuGroup`의 식별자(`id`)인 `menuGroupId`를 가진다.
* 손님에게 제공하거나 제공하지 않을 수 있도록 메뉴 노출 여부(`displayed`)를 가진다. 
* 메뉴에 속한 상품(`MenuProduct`)의 목록을 가진다.
    * `MenuProduct`은 식별자(`seq`)를 가진다.
    * `MenuProduct`은 어떤 상품이 속해 있는지 상품의 식별자(`id`)인 `productId`를 가진다.
    * `MenuProduct`은 0개 이상의 상품 수량(`quantity`)을 가진다.

#### 기능/조건
* 메뉴에 속한 상품 금액의 총합을 알려준다.
* 유효한 가격인지 알려준다.
    * 메뉴 가격은 0원 이상, 메뉴에 포함된 상품들의 가격과 갯수를 곱한 총액보다 작거나 같아야 한다.
* 메뉴를 등록한다.
    * 메뉴는 0원 이상의 가격을 가진다.
    * 메뉴는 특정 `MenuGroup`에 속해야 한다.
    * 메뉴명은 비워둘 수 없다.
    * 메뉴명에 비속어가 포함될 수 없다.
        * 비속어 검증기(`PurgomalumClient`)를 통해 이름에 비속어가 포함되어 있는지 확인한다.
    * 메뉴에 담을 상품(`MenuProduct`) 목록은 비워둘 수 없고, 1개 이상의 등록된 상품(`Prodcut`)이 있어야 한다.
    * 메뉴 가격이 유효한 가격일 경우에만 등록할 수 있다.
* 메뉴의 가격을 변경한다.
    * 메뉴 가격이 유효한 가격일 경우에만 변할 수 있다.
* 메뉴 가격을 노출시킨다.
    * 메뉴 가격이 유효하지 않을 경우 노출할 수 없다.
* 메뉴를 숨긴다.
* 메뉴 목록을 조회한다.

### 주문 테이블(OrderTable) Context
#### 속성
* 식별자(`id`)를 가진다.
* 외부에 노출되는 주문테이블명(`name`)을 가진다.
* 방문한 손님 수(`numberOfGuests`)를 가진다.
* 테이블이 비워져있는지 여부를 나타내는 `empty`를 가진다.

#### 기능/조건
* 주문 테이블을 등록한다.
    * 주문 테이블명은 비워둘 수 없다.
    * 주문 테이블명에 비속어가 포함될 수 없다.
        * 비속어 검증기(`PurgomalumClient`)를 통해 이름에 비속어가 포함되어 있는지 확인한다.
    * 새로 추가되는 주문 테이블은 비어있으며, 방문 손님 수는 0명이다.
* 주문 테이블에 손님이 앉는다.
    * 테이블이 비어있는 상태가 아님을 표시한다.
* 주문 테이블을 정리한다.
    * 완료(`COMPLETED`)되지 않은 상태(`OrderStatus`)의 주문이 있는 주문 테이블은 빈 테이블로 설정할 수 없다.
    * 테이블이 비어있는 상태임을 표시한다.
    * 손님이 0명인 상태임을 표시한다.
* 방문한 손님 수를 변경한다.
    * 빈 테이블은 방문한 손님 수를 변경할 수 없다.
    * 방문한 손님 수는 0 이상 이어야 한다.
* 주문 테이블의 목록을 조회한다.

### 주문(Order) Context
#### 속성
* 식별자(`id`)를 가진다.
* 어떤 주문인지 나타내는 주문 유형(`OrderType`)을 가진다.
    * 배달 주문(`DELIVERY`), 포장 주문(`TAKEOUT`), 매장 주문(`EAT_IN`) 타입이 있다.
* 주문 처리가 어디까지 이루어졌는지 현재의 상태를 나타내는 주문 상태(`OrderStatus`)를 가진다.
    * 접수 대기(`WAITING`), 접수(`Accepted`), 제공 완료(`SERVED`), 배달 중(`DELIVERING`), 배달 완료(`DELIVERED`), 주문처리 완료(`COMPLETED`) 가 있다.
* 주문 일시를 나타내는 `orderDateTime`을 가진다.
* 주문한 메뉴를 의미하는 주문 항목(`OrderLineItem`) 목록인 `orderLineItemRequests`를 가진다.
    * `OrderLineItem`은 식별자(`seq`)를 가진다.
    * `OrderLineItem`은 어떠한 메뉴가 담겨 있는지 메뉴의 식별자(`id`)인 `MenuId`를 가진다.
    * `OrderLineItem`은 주문한 메뉴별 주문항목 수량(`quantity`)을 가진다.
    * `OrderLineItem`은 결제 가격(`price`)를 가진다.

#### 기능/조건
- 주문을 등록한다.
    - 주문 유형(`OrderType`)이 올바르지 않으면 등록할 수 없다.
    - 1개 이상의 등록된 `Menu`로 주문을 등록할 수 있다.
    - 매장 주문(`EAT_IN`) 유형의 주문은 주문 항목(`OrderLineItem`)의 수량(`quantity`)이 0 미만일 수 있다.
    - 매장 주문(`EAT_IN`) 유형을 제외한 주문의 경우 주문 항목(`OrderLineItem`)의 수량(`quantity`)은 0 이상이어야 한다.
    - 없는 `Menu`의 주문은 등록할 수 없다.
    - 숨겨진(`hide`) 메뉴는 주문할 수 없다.
    - 주문한 메뉴(`OrderLineItem`)의 결제 가격(`price`)은 실제 메뉴(`Menu`) 가격(`price`)과 일치해야 한다.
    - 주문 등록 직후 `OrderStatus`는 `WAITING`상태이다.
    - 주문 시각(`orderDateTime`)은 현재 시각으로 등록한다.
    - 배달 주소(`deliveryAddress`)가 올바르지 않으면 배달 주문(`DELIVERY`)을 등록할 수 없다.
        - 배달 주소는 비워 둘 수 없다.
    - 매장 주문(`EAT_IN`) 유형의 주문은 주문 테이블(`OrderTable`) 정보가 올바르지 않으면 등록할 수 없다.
         - 존재하는 주문 테이블에 매장 주문을 등록할 수 있다.
         - 빈(`empty`) 테이블에는 매장 주문을 등록할 수 없다.
- 주문을 접수한다.
    - `WAITING` 상태인 주문만 접수할 수 있다.
    - `DELEVERY` 유형의 주문을 접수하면, 배달 대행사(`KitchenridersClient`)를 호출한다.
        * `KitchenridersClient`에게 주문번호(`orderId`), 결제금액(`amonut`), 배달지(`address`) 정보를 전달한다.
    - 주문 상태를 `ACCEPTED`로 변경한다.
- 주문을 서빙한다.
    - `ACCEPTED` 상태인 주문만 서빙할 수 있다.
    - 주문 상태를 `SERVED`로 변경한다.
- 주문을 배달한다.
    - `DELEVERY` 유형의 주문만 배달할 수 있다.
    - `SERVED` 상태의 주문만 배달할 수 있다.
    - 주문 상태를 `DELIVERING`로 변경한다.
- 주문을 배달 완료한다.
    - `DELIVERING` 상태의 주문만 배달 완료할 수 있다.
    - 주문 상태를 `DELIVERED`로 변경한다.
- 주문을 완료한다.
    - `DELEVERY` 주문의 경우 `DELIVERED` 상태의 주문만 완료할 수 있다.
    - `TAKEOUT` 또는 `EAT_IN` 주문의 경우 `SERVED`상태의 주문만 완료할 수 있다.
    - 주문 상태를 `COMPLETED`로 변경한다. 
    - `EAT_IN` 유형의 주문인 경우, 
        - 해당 주문을 받은 주문 테이블(`OrderTable`)의 모든 `EAT_IN` 주문이 완료(`COMPLETED`)되면 빈 테이블로 설정한다.(`empty`)
        - 완료되지 않은 `EAT_IN` 주문이 있는 주문 테이블(`OrderTable`)은 빈 테이블로 설정하지 않는다.
- 주문 목록을 조회할 수 있다.

![image](https://user-images.githubusercontent.com/35985636/130323613-b62c53d8-7092-4310-a510-311c48714872.png)
