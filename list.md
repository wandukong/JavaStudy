# List
>  객체를 일렬로 늘어놓은 구조다.
- 순서를 유지하고 저장한다.
 - 중복 허용
 - 가변 길이 (배열은 고정 길이다. List와 Array의 차이점)
 - ArrayList, Vector, LinkedList, Stack, Queue 등이 있다.

## 🏃‍♂️ArrayList
- 비동기화 (비동기화이기 때문에 Vector보다 빠르다. Vector는 동기화이다. )
 - 데이터 검색 시 굉장히 빠르다. get(int index)를 통해 O(1)의 시간 복잡도
 - 일반적으로 데이터 삽입/삭제에 LinkedList에 비해 느리다. 최악의 경우 O(N)의 시간 복잡도
-  대량의 데이터 삽입/삭제에 수월하다. (소량은 LinkedList가 빠르다)

## 🧘‍♂️Vector
- 동기화 (동기화이기 때문에 ArrayList보다 느리다.
 - 데이터 검색 시 굉장히 빠르다. get(int index)를 통해 O(1)의 시간 복잡도
 - 일반적으로 데이터 삽입/삭제에 LinkedList에 비해 느리다. 최악의 경우 O(N)의 시간 복잡도
-  대량의 데이터 삽입/삭제에 수월하다. (소량은 LinkedList가 빠르다)

## 🏄‍♂️LinkedList
- 데이터 삽입/삭제에 수월하다. (대량의 데이터는 삽입/삭제에 어려움)
	-> LinkedList는 이전 노드와 다음 노드를 참조하는 상태만 변경하면 되기 때문이다.  
		  삽입/삭제가 일어날 때 O(1)의 시작 복잡도
- 데이터 검색 시 모든 요소를 탐색해야 하기 때문에 최악의 경우에는 O(N)의 시간 복잡도


## 🏊‍♀️메소드
**선언**
```java
ArraryList<자료형> al = new ArrayList<자료형>();
ArraryList<자료형> al = new ArrayList<자료형>(3); // (초기용량)
ArraryList<자료형> al = new ArrayList<자료형>(3,4); // (초기용량, 증가용량)
```
<hr />

**객체 검색**
```java
al.get(5); // 해당 인덱스에 저장된 데이터 반환
al.indexOf(12.34); // 해당 데이터 인덱스 조사
al.lastIndexOf(12.34); // 해당 데이터 인덱스 조사 (뒤에서 부터 검색)
al.contains("자바"); // 해당 데이터 존재하는지 true/false 
al.containsAll(al2); // 해당 리스트의 모든 데이터 존재하는지 true/false 
```

**객체 추가**
```java
al.add(2); 
al.addElement("자바")
al.add(2,"열공"); // 해당 인덱스에 데이터 추가
```
<hr />

**객체 수정**
```java
al.set(2, "자바"); // 해당 인덱스에 데이터 설정
al.setElement("자바",2);  
```
<hr />

**객체 삭제**
```java
al.remove(3); // 해당 인덱스에 데이터 삭제
al.removeElement(3); // 해당 인덱스에 데이터 삭제
al.clear();  // 모든 데이터 삭제
al.removeAllElements();  // 모든 데이터 삭제
```
<hr />

**리스트 비었는지 확인**
```java
al.isEmpty(); // 비어있는지 조사
```
<hr />


**부분 리스트 반환**
```java
al.subList(1,4); // 리스트의 인덱스 1~3번 데이터 반환, 4는 미포함
```
<hr />

**데이터가 존재하는 크기 확인**
```java
al.size();
```
<hr />

**할당된 메모리 크기 확인**
```java
al.capacity();
```
<hr />

**비어 있는 메모리 삭제**
```java
al.trimToSize();
```
