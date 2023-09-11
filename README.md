# 키친포스

## 퀵 스타트

```sh
cd docker
docker compose -p kitchenpos up -d
```

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

### 상품 도메인
| 한글명   | 영문명           | 설명                 |
|-------|---------------|--------------------|
| 상품    | Product       | 판매하는 음식 종류         |
| 상품명   | Product Name  | 상품의 이름             |
| 상품 가격 | Product Price | 0원 이상의 상품 가격       |
| 비속어   | Profanity     | 상품 이름에 포함될 수 없는 단어 |

### 메뉴 도메인
| 한글명   | 영문명                    | 설명                                                       |
|-------|------------------------|----------------------------------------------------------|
| 메뉴 그룹 | Menu Group | 각 메뉴를 그룹화하는데 사용되는 범주                                     |
| 메뉴 그룹명 | Menu Group Name | 메뉴 그룹의 이름                                                |
| 메뉴 | Menu | 가게에서 제공하는 음식 메뉴로 1개 이상의 상품으로 구성 |
| 메뉴 명 | Menu Name | 메뉴의 이름                                                   |
| 메뉴 가격 | Menu Price | 0원 이상의 메뉴 가격                                             |
| 비속어  | Profanity     | 메뉴 이름에 포함될 수 없는 단어                                       |
| 미노출 메뉴 | Not Displayed Menu | 메뉴의 가격이 메뉴에 속한 상품 금액의 합보다 높을 경우 노출되지 않는 메뉴로 설정됨 |

### 주문 도메인 (공통)
| 한글명    | 영문명                | 설명                                                              |
|--------|--------------------|-----------------------------------------------------------------|
| 주문     | Order              | 고객이 음식을 요청하고 전달 받기까지의 프로세스                                      |
| 주문 항목  | Order Line Item    | 주문에 포함된 메뉴                                                      |
| 주문 가격  | Order Price        | 주문한 메뉴의 가격에 주문 수량을 곱한 총 금액                                      |
| 주문 수량  | Order Quantity     | 주문한 메뉴의 수량                                                      |
| 주문 유형  | Order Type         | 주문의 유형으로 매장, 배달, 포장 중 한가지                                       |
| 주문 상태  | Order Status       | 주문의 현재 상태로 대기, 수락, 서빙, 배달시작, 배달완료, 주문완료 중 한가지                   |
| 주문 대기  | Order Waiting      | 주문을 받고 수락하기 전까지의 대기하는 상태                                        |
| 주문 수락  | Order Accept       | 대기 중인 주문을 수락한 상태                                                |
| 주문 서빙  | Order Serving      | 주문된 음식이 조리 완료되어 매장 직원이나 배달 기사가 손님에게 전달하기 직전의 상태로 수락된 주문에 한해서 가능 |
| 주문 완료  | Order Completion   | 주문한 음식이 고객에게 인도되어 주문이 완료된 상태                                    |

#### 매장 주문
| 한글명       | 영문명                    | 설명                                   |
|-----------|------------------------|--------------------------------------|
| 매장 주문     | Eat In Order | 매장에서 식사하는 주문                         |
| 주문 테이블    | Order Table | 음식점에서 손님들이 식사를 하는 테이블                |
| 테이블명      | Table Name | 주문 테이블의 이름                           |
| 테이블 점유 상태 | Table Occupancy Status | 손님이 앉아 있는지 또는 테이블이 비어 있는지 알려주는 주문 테이블의 상태 |
| 빈 테이블     | Empty Table | 주문 테이블의 점유 상태가 미점유인 상태               |
| 방문한 손님 수  | Number of Guests | 주문 테이블에 착석한 0명 이상의 손님 수              |

#### 배달 주문
| 한글명 | 영문명 | 설명                              |
| --- | --- |---------------------------------|
| 배달 주문 | Delivery Order | 배달 주소로 배달하는 주문                  |
| 배달 주소 | Delivery Address | 배달 주문의 음식을 전달 할 배달 주소           |
| 배달 대행사 | Delivery Agency | 배달 주문된 음식을 손님에게 직접 배달하는 회사      |
| 배달 호출 | Delivery Call | 배달 대행사에게 배달 주문정보를 전달하는 것        |
| 배달 시작 | Delivery Start | 배달 주문의 시작 상태으로 수락된 주문에 한해서 가능   |
| 배달 완료 | Delivery Complete | 주문을 배달 완료한 상태로 배달 시작한 주문에 한해서 가능 |                           

#### 포장 주문
| 한글명 | 영문명 | 설명 |
| --- | --- |----|
| 포장 주문 | Take Out Order | 포장해서 가져가는 주문                |

## 모델링
### 상품
#### 속성
- `Product`는 식별자를 가진다.
- `Product`는 `Product Name`을 가진다.
- `Product`는 `Product Price`를 가진다.
#### 행위
- `Product`를 생성한다.
- `Product Price`를 변경한다.
- 생성한 `Product` 목록을 조회한다.
#### 정책
- `Product Name`은 비워두거나 `Profanity`를 포함할 수 없다.
- `Product Price`는 0원 이상이어야 한다.

### 메뉴 그룹
#### 속성
- `MenuGroup`은 식별자를 가진다.
- `MenuGroup`은 `MenuGroup Name`을 가진다.
#### 행위
- `MenuGroup`을 생성한다.
- 생성한 `MenuGroup`의 목록을 조회한다.
#### 정책
- `MenuGroup Name`은 비워둘 수 없다.

### 메뉴
#### 속성
- `Menu`는 식별자를 가진다.
- `Menu`는 `Menu Name`을 가진다.
- `Menu`는 `Menu Price`를 가진다.
- `Menu`는 `MenuGroup`을 가진다.
- `Menu`는 `노출 여부`를 가진다.
- `Menu`는 `MenuProduct`를 가진다.
- `MenuProduct`는 식별자를 가진다.
- `MenuProduct`는 `Product`를 가진다.
- `MenuProduct`는 `Quantity`를 가진다.
#### 행위
- `Menu`를 생성한다.
- `Menu Price`를 변경한다.
- `Menu`를 노출한다.
- `Menu`를 숨긴다.
- 생성한 `Menu`의 목록을 조회한다.
#### 정책
- `Menu Price`는 0원 이상이어야 한다.
- `Menu Name`은 비워두거나 `Profanity`를 포함할 수 없다.
- `Menu`는 하나의 `MenuGroup`에 속해야 한다.
- `Menu`는 `MenuProduct`를 1개 이상 가지고 있어야 한다.
- `MenuProduct`의 `Quantity`는 0개 이상이어야 한다.
- `Menu Price`는 `MenuProduct`의 가격의 합보다 적거나 같아야 한다.
- `Menu Price`가 `MenuProduct`의 가격의 합보다 크면 `NotDisplayedMenu`로 설정된다.

### 주문 - 공통
#### 속성
- `Order`는 식별자를 가진다.
- `Order`는 `OrderType`을 가진다.
- `Order`는 `OrderStatus`를 가진다.
- `Order`는 `주문일시`를 가진다.
- `Order`는 `OrderLineItem`을 가진다.
- `OrderLineItem`은 식별자를 가진다.
- `OrderLineItem`은 `Menu`를 가진다.
- `OrderLineItem`은 `Price`를 가진다.
- `OrderLineItem`은 `Quantity`를 가진다.
#### 행위
- `Order`를 생성한다.
- `OrderStatus`를 `OrderWaiting`, `OrderAccept`, `OrderServing`, `DeliveryStart`, `DeliveryComplete`, `OrderCompletion` 중 하나로 변경한다.
- 생성한 `Order`의 목록을 조회한다.
#### 정책
- 생성된 `Order`는 `OrderStatus`가 `OrderWaiting`으로 설정된다.
- `OrderType`은 `Eat In Order`, `Take Out Order`, `Ddelivery Order` 중 하나다.
- `OrderStatus`는 `OrderWaiting`, `OrderAccept`, `OrderServing`, `DeliveryStart`, `DeliveryComplete`, `OrderCompletion` 중 하나다.
- `OrderStatus`가 `OrderWaiting`일 경우만 `OrderAccept`로 변경할 수 있다.
- `OrderStatus`가 `OrderAccept`일 경우만 `OrderServing`으로 변경할 수 있다.
- `Menu Price`가 `OrderLineItem`의 `Price`와 같아야 주문할 수 있다.
- `OrderLineItem`을 1개 이상 가지고 있어야 한다.

### 주문 - 배달 주문
#### 속성
- `Order`는 `DeliveryAddress`를 가진다.
#### 행위
- `OrderStatus`를 `DeliveryStart`, `DeliveryComplete` 중 하나로 변경한다.
- `DeliveryAgency`에 `DeliveryCall`을 한다.
#### 정책
- 배달 주문은 `OrderStatus`의 변경 순서가 `OrderWaiting` -> `OrderAccept` -> `OrderServing` -> `DeliveryStart` -> `DeliveryComplete` -> `OrderCompletion` 순이다.
- 배달 주문은 `DeliveryAddress`를 비워둘 수 없다.
- 배달 주문만 `DeliveryStart`로 설정할 수 있다.
- 배달 주문만 `DeliveryCall`을 한다.
- `OrderStatus`가 `OrderServing`일 경우만 `DeliveryStart`로 설정할 수 있다.
- `OrderStatus`가 `DeliveryStart`일 경우만 `DeliveryComplete`로 설정할 수 있다.
- `OrderStatus`가 `DeliveryComplete`일 경우만 `OrderCompletion`로 설정할 수 있다.
- `OrderLineItem`의 수량은 0개 이상이다.

### 주문 - 매장 주문
#### 속성
- `Order`는 `OrderTable`을 가진다.
- `OrderTable`은 식별자를 가진다.
- `OrderTable`은 `Order Table Name`을 가진다.
- `OrderTable`은 `Table Occupancy Status`를 가진다.
- `OrderTable`은 `Number Of Guests`를 가진다.
#### 행위
- `OrderTable`을 생성한다.
- `OrderTable`의 `Number Of Guests`를 변경한다.
- `OrderTable`을 `Occupancy Status`를 설정한다.
#### 정책
- 매장 주문은 `OrderStatus`의 변경 순서가 `OrderWaiting` -> `OrderAccept` -> `OrderServing` -> `OrderCompletion` 순이다.
- `OrderStatus`가 `OrderServing`일 경우만 `OrderCompletion`으로 설정할 수 있다.
- `OrderTable`의 `Order Table Name`은 비워둘 수 없다.
- `OrderTable`의 `Number Of Guests`는 0 이상이어야 한다.
- `OrderLineItem`의 수량은 0보다 작을 수 있다.

### 주문 - 포장 주문
#### 속성
- `Order`는 `OrderType`이 `Take Out Order`일 경우 `Order Quantity`가 0 이상이어야 한다.
#### 정책
- 포장 주문은 `OrderStatus`의 변경 순서가 `OrderWaiting` -> `OrderAccept` -> `OrderServing` -> `OrderCompletion` 순이다.
- `OrderStatus`가 `OrderServing`일 경우만 `OrderCompletion`로 변경할 수 있다.
- `OrderLineItem`의 수량은 0개 이상이다.
