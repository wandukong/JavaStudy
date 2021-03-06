
# Class

## π©μμ (inheritance)
> κΈ°μ‘΄ ν΄λμ€λ₯Ό **νμ₯**ν΄μ μλ‘μ΄  ν΄λμ€λ₯Ό λ§λλ κΈ°μ 
- extends
- λ¨μΌ μμλ§ μ§μ
- final classλ μμ κΈμ§ 
- λΆλͺ¨ ν΄λμ€λ₯Ό μμ λ°μ λ, λΆλͺ¨ ν΄λμ€μ μμ±μ ν¨μκ° λ¨Όμ  μ€νλλ€.

> **override** : λΆλͺ¨ν΄λμ€λ‘λΆν° μμλ°μ λ©μλλ₯Ό μ¬μ μνλ κ². μμ κ°μ²΄μμ μ€λ²λΌμ΄λ©ν λ©μλλ νΈμΆμ μ€λ²λΌμ΄λ©ν λ©μλκ° μ°μ μ λμ΄ νΈμΆλ¨ (λμΌν λ¦¬ν΄νμ, λ©μλ μ΄λ¦, λ§€κ°λ³μλ₯Ό κ°μ ΈμΌν¨)

> **overload** : λ©μλμ μ΄λ¦μ κ°κ³ , λ§€κ°λ³μλ₯Ό λ€λ₯΄κ² ν¨μΌλ‘μ¨ μ¬λ¬ λ©μλλ₯Ό λ§λλ κ²


## π°μΆμ ν΄λμ€ (Abstract Class)
> ν΄λμ€μ κ³΅ν΅μ μΈ λΆλΆμ μΆμΆν΄ μ΄λμ λ κ·κ²©μ μ‘μλμ μΆμμ μΈ ν΄λμ€μ΄λ€
-  μμμ κ°μ νκΈ° μν¨μ΄λ€. λΆλͺ¨ ν΄λμ€μμ μ μλ§ νκ³ , μ€μ  λμμ μμ ν΄λμ€μμ νκ² λλ€.
- μΆμ ν΄λμ€λ μΌλ° λ©μλμ μΌλ° λ³μλ₯Ό κ°μ§ μ μλ€.
- μμ²΄μ μΌλ‘ μΈμ€ν΄μ€λ₯Ό μμ±ν  μ μλ€.
- μ μΈ μ ν€μλ abstractλ₯Ό μ¬μ©νλ€.
- μμ μ extendsλ₯Ό μ¬μ©νλ€.

```java
abstract class Animal{
	abstract void bark(); // μΆμ λ©μλ
	void feed(){ // μΌλ° λ©μλ
		...
	}
}
```
```java
class Dog extends Animal{
	void bark(){ // μΆμ λ©μλ κ΅¬ν
		...
	}
}
```

### νλ³ν
```java
public abstract class Shape { // μΆμ ν΄λμ€
	double result = 0;
	public abstract double calc();
	public abstract void show(String name);
	
	public void go() {
		System.out.println("κ°μμ");
	}
}
```
```java
public class Circle2 extends Shape{

	double r = 5.0;
	
	@Override
	public double calc() {
		result = r*r*Math.PI;
		return result;
	}

	@Override
	public void show(String name) {
		calc();
		System.out.println(name + "μ λμ΄ : " + result + "μΈ "+ name +"μ κ·Έλ Έμ΅λλ€.");
	}
	
	public void draw() {
		calc();
		System.out.println("μμ λμ΄ : " + result + "μΈ μμ κ·Έλ Έμ΅λλ€.");
	}
}

```
```java
// 1. κ° ν΄λμ€λ‘ κ°μ²΄ μμ± λ°©λ²
System.out.println("===λ°©λ²1===");
Triangle t = new Triangle(); // λ¨ μμ λ°μ μμ ν΄λμ€λ‘λ κ°μ²΄λ₯Ό μμ±ν  μ μλ€.
t.draw();

// 2. Shape λΆλͺ¨ μΆμ ν΄λμ€ μ΄μ©ν΄μ κ°μ²΄ μμ±νκΈ° 
System.out.println("===λ°©λ²2===");
Shape s = new Circle2();
s.show("Circle"); 	// μ€λ²λΌμ΄λ©λ λ©μλλ μ¬μ© κ°λ₯
s.go(); 			// λΆλͺ¨ ν΄λμ€μ λ©μλ
// s.draw(); μλ¬    // μμ ν΄λμ€μλ§ μμ±λ λ©μλ
```

## πͺμΈν°νμ΄μ€ (Interface)
> μΈν°νμ΄μ€λ ν΄λμ€λ€μ΄ κ΅¬νν΄μΌ νλ λμμ μ§μ νλλ° μ¬μ©λλ μΆμ μλ£νμ΄λ€.
- ν΄λμ€κ° μλλ€.
- μΆμ λ©μλμ, final λ³μ(μμ)λ§μ κ°μ§ μ μλ€.
- μΈν°νμ΄μ€λ₯Ό κ΅¬νν ν΄λμ€λ λͺ¨λ  λ©μλλ₯Ό κ°μ μ μΌλ‘ κ΅¬νν΄μΌνλ€.
- μΈν°νμ΄μ€ κ°μ μμλ extendsλ₯Ό μ¬μ©νλ€.
- λ€μ€ κ΅¬ν
- μ μΈ μ ν€μλ interfaceλ₯Ό μ¬μ©νλ€.
- κ΅¬ν μ ν€μλ implementsλ₯Ό μ¬μ©νλ€.

```java
interface A{ 
	int x = 90; // final static int x = 90; μ κ°μ κ²μ΄λ€.
	final int y = 77;  // λ³μκ° italic μ²΄λ‘ λμ λ²λ¦Ό -> final static λ³μ

	// abstract method λ§ κ°λλ€. - abstract μλ΅ κ°λ₯ν¨
	public void show(); // public abstract void show(); μ κ°μ
	public abstract void disp();
}
```

```java
interface D extends A{ // μΈν°νμ΄μ€ κ°μ μμλ extendsλ₯Ό μ¬μ©νλ€
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
class Multi extends S implements B,C,A{ // λ¬΄μ‘°κ±΄ extends λ¨Όμ  μ μΈνκ³ , implementsκ° μ μΈλμ΄μΌ νλ€.

	@Override
	public void draw() {} // interface C

	@Override
	public void bView() {} // interface B

	@Override
	public void show() {} // interface A
	
	@Override
	public void disp() {}  // interface A
}
```

### νλ³ν
```java
class R implements D{
	@Override
	public void bView() {}
	
	@Override
	public void dView() {}
	
	public void rVeiw() {
		System.out.println("Rect view");
	}
}
```

```java
public static void main(String[] args)
{
	// 1. μμ μΌλ‘ κ°μ²΄ μμ±
	R r1 = new R();
	
	// 2. λΆλͺ¨λ‘ κ°μ²΄ μμ± (νλ³ν : μ μΊμ€ν)
	D r2 = new R();
	B r3 = new R();
	// r2.rView(); μμμ λ©μλλ μ¬μ©ν  μ μλ€.
	// r3.rView(); μμμ λ©μλλ μ¬μ©ν  μ μλ€.
}
```