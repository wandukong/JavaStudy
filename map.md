
# Map
> Map은 key와 value로 구성된 객체를 저장하는 자료구조이다.
- Key는 중복 저장될 수 없지만, value는 중복 저장할 수 있다.
- HashMap, HashTable, TreeMap
- iterator와 get()을 결합하여 데이터를 찾는다.


## 🏡HashMap
- 비동기화
- null 허용 

## 🏢HashTable
- 동기화
- null 허용x

## 🏰TreeMap
- key를 기준으로 자동으로 정렬된다.

## 🏫메소드
 


**선언**
```java
Map<키자료형,값자료형> map = new HashMap<키자료형,값자료형>();
```
<hr />

**객체 삽입**
```java
map.put("kosa", "th2");
```
<hr />

**값 얻기**
```java;
map.get(key);
```
<hr />

**맵 탐색**
```java
Iterator it = map.entrySet().iterator(); 
while(it.hasNext()) {
	Map.Entry e = (Map.Entry)it.next();
	System.out.println("회사 명 : " + e.getKey() + ", 기수 : " + e.getValue());
}
```
```java
for(Map.Entry entry : m.entrySet()) {
	System.out.println("이름  : " + entry.getKey() + ", 키 : " + entry.getValue());
}
```
<hr />

**맵 크기 확인**
```java
map.size();
```
<hr />

**객체 삭제**
```java
map.remove(key);
```
<hr />

**객체 비어있는지 확인**
```java
map.isEmpty();
```
<hr />


**키와 값 반환**
```java
Set set = map.entrySet(); // key와 value를 반환한다.
```