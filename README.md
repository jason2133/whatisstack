# whatisstack

# 스택이란 무엇인가

## 스택 Stack
[영어사전] Stack : 쌓다, 쌓아올린 더미

스택이란, 데이터의 삽입과 삭제가 한쪽 방향에서만 일어나는 구조
자료를 누적시키고 필요할 때 빼내되, 처음의 것이 아니라 최근의 것을 빼내는 형식
-> 가장 마지막에 누적된 것이 가장 먼저 접근되는 형태의 자료구조
-> 한 쪽 끝에서만 항목을 삭제하거나 새로운 항목을 저장하는 자료구조


## 특징
- 한 쪽으로만 데이터가 들어간다
- 한 쪽으로만 들어가기 때문에 처음 들어간 것은 밑에 깔려서 나중에 나올 수밖에 없다 (FILO 구조 – First In Last Out)
- 반대로 (LIFO 구조 – Last In First Out) 마지막에 들어간 것은 첫 번째로 나오겠지.

ex. 스택 그림
| D |
| C |
| B |
| A |
----- ← 여긴 막혀있음

- PUSH (삽입) : 스택에 자료를 넣는 것을 PUSH라고 한다 (위에서 A, B, C, D 등을 스택에 넣는 행위)
- POP (삭제) : 스택에 자료를 빼내는 것을 POP이라고 한다 (맨 위에 자료 D부터 하나씩 제거하는 행위)
- TOP (맨위) : 스택의 제일 위에 있는 자료를 TOP라고 한다 (맨 위에 있는 자료인 D가 TOP)
- BOTTOM (맨아래) : 스택의 제일 아래에 있는 자료를 BOTTOM이라고 한다. (맨 밑에 있는 자료인 A가 BOTTOM)
- PEEK (읽기) : 마지막 위치(TOP)에 해당하는 데이터를 읽음. 이때 TOP의 변화는 없음.
- 스택이 담을 수 있는 사이즈 이상을 PUSH할 때에는 Overflow가 발생한다
- 스택에서 자료가 전부 POP 되고 자료가 더 이상 없는 공백 상태일 때, POP이 호출되면 Underflow가 발생한다

### 스택의 연산
- is_empty(s) : 스택이 공백상태인지 검사
- is_full(s) : 스택이 포화상태인지 검사
- create() : 스택을 생성
- peek(s) : 요소를 스택에서 삭제하지 않고 보기만 하는 연산

### 스택 구현 – 스택은 Array나 LinkedList 방식으로 구현이 가능함

## 장점
- 단지 현 경로 상의 노드들만 기억하면 되므로 저장공간의 수요가 비교적 적다
- 목표노드가 깊은 단계에 있을 경우 해를 빨리 구할 수 있다
- 크기가 제한되지 않음
- 구현이 쉽다
- 이해하기 쉽다
- 코딩이 쉽다

## 용도
- 지역변수 저장이 주용도임.
- 함수의 콜스택에 쓰임
- 함수가 함수를 호출하거나 자기 자신을 호출하는 것도 스택에 기반을 두고 있음
- 문자열을 역순으로 출력할 때
- 연산자 후위표기법
- 임시 데이터 백업
- 함수 매개변수 전달
- 함수 호출관련 정보

√ 컴퓨터에서는 스택을 언제 활용할까?
- 응용프로그램을 사용하여 문서편집 혹은 그림편집 중 방금 한 작업을 취소하기 위해 사용하는 되돌리기 기능
- 웹 브라우저에서도 방금 전 방문했던 사이트들의 기록을 저장해 두었다가 ‘이전 페이지로 돌아가기’ 기능
