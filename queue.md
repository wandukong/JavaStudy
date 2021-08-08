# Queue
> 선입선출(FIFO)인 자료 구조이다.
```java
Queue<자료형> q = new Queue<자료형>(); // 선언
q.offer(데이터); // 데이터 추가
while(!q.empty()){
	System.out.println(q.poll());  // 데이터 반환
}
```
```java
q.peek(); // 큐의 맨 앞 객체를 반환한다. 큐에서 객체를 제거하지 않는다.
q.poll(); // 스택의 맨 앞 객체를 반환한다. 큐에서 객체를 제거한다.
```