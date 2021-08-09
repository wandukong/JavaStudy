# set
> set이란 수학에서의 집합과 비슷한 개념이다.
- 순서 없이 저장한다.
- 중복 허용 X
- iterator를 통해 데이터를 찾는다.
- HashSet, TreeSet
- TreeSet은 자동 정렬한다.

## 👊메소드
**선언**
```java
HashSet<자료형> hs = new HashSet<자료형>();
```
<hr />

**객체 추가**
```java
hs.add("키보드");
```
<hr />

**셋 검색**
```java
Iterator it = hs.iterator();
while(it.hasNext()){
	System.out.println(it.next());
}
```
```java
for(String item : hs){
	System.out.println(item);
}
```
<hr />

**셋 접근**
```java
hs.contains("볼펜"); // 해당 데이터 존재하는지 true/false
```
<hr />


**객체 크기**
```java
hs.size(); 
```
<hr />

**셋 비었는지 확인**
```java
hs.isEmpty(); 
```
<hr />

**셋 비우기**
```java
hs.clear(); 
```
<hr />

**TreeSet.headSet()**
> 기준보다 작은 값
```java
ts.headSet(50); // [10,35,45]
```
<hr />

**TreeSet.tailSet()**
> 기준보다 같거나 큰 값
```java
ts.tailSet(50); // [50,65,85,95,100]
```