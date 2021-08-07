# Class

## 🍩상속 (inheritance)
> 기존 클래스를 **확장**해서 새로운  클래스를 만드는 기술
- extends
- 단일 상속만 지원
- final class는 상속 금지 
- 부모 클래스를 상속 받을 때, 부모 클래스의 생성자 함수가 먼저 실행된다.

> **override** : 부모클래스로부터 상속받은 메소드를 재정의하는 것. 자식 객체에서 오버라이딩한 메소드는 호출시 오버라이딩한 메소드가 우선시 되어 호출됨 (동일한 리턴타입, 메소드 이름, 매개변수를 가져야함)

> **overload** : 메소드의 이름은 같고, 매개변수를 다르게 함으로써 여러 메소드를 만드는 것


## 🍰추상 클래스 (Abstract Class)
> 클래스의 공통적인 부분을 추출해 어느정도 규격을 잡아놓은 추상적인 클래스이다
-  상속을 강제하기 위함이다. 부모 클래스에서 정의만 하고, 실제 동작은 자식 클래스에서 하게 된다.
- 추상 클래스는 일반 메소드와 일반 변수를 가질 수 있다.
- 자체적으로 인스턴스를 생성할 수 없다.
- 선언 시 키워드 abstract를 사용한다.
- 상속 시 extends를 사용한다.

```java
abstract class Animal{
	abstract void bark(); // 추상 메소드
	void feed(){ // 일반 메소드
		...
	}
}
```
```java
class Dog extends Animal{
	void bark(){ // 추상 메소드 구현
		...
	}
}
```

## 🍪인터페이스 (Interface)
> 인터페이스는 클래스들이 구현해야 하는 동작을 지정하는데 사용되는 추상 자료형이다.
- 클래스가 아니다.
- 추상 메소드와, final 변수(상수)만을 가질 수 있다.
- 인터페이스를 구현한 클래스는 모든 메소드를 강제적으로 구현해야한다.
- 인터페이스 간의 상속도 extends를 사용한다.
- 다중 구현
- 선언 시 키워드 interface를 사용한다.
- 구현 시 키워드 implements를 사용한다.

```java
interface A{ 
	int x = 90; // final static int x = 90; 와 같은 것이다.
	final int y = 77;  // 변수가 italic 체로 누워 버림 -> final static 변수

	// abstract method 만 갖는다. - abstract 생략 가능함
	public void show(); // public abstract void show(); 와 같음
	public abstract void disp();
}
```

```java
interface D extends A{ // 인터페이스 간의 상속도 extends를 사용한다
	void dView();
}
```

```java
interface B{
	void bView();
}

interface C{
	String name = "happy";
	public void draw();
}
```

```java 
class Multi extends S implements B,C,A{ // 무조건 extends 먼저 선언하고, implements가 선언되어야 한다.

	@Override
	public void draw() { // interface C
		...
	}

	@Override
	public void bView() { interface B
		...
	}

	@Override
	public void show() { // interface A
		...
	}
	@Override
	public void disp() { // interface A
		...
	}
}
```