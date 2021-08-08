# Stack 
> 후입선출(LIFO)인 자료 구조이다.
```java
Stack<자료형> st = new Stack<자료형>(); // 선언
st.push(데이터); // 데이터 추가
while(!st.empty()){
	System.out.println(st.pop());  // 데이터 반환
}
```
```java
st.peek(); // 스택의 맨 위 객체를 반환한다. 스택에서 객체를 제거하지 않는다.
st.pop(); // 스택의 맨 위 객체를 반환한다. 스택에서 객체를 제거한다.
```