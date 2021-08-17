
# Static

## 🍒static field
> static field를 사용하면, 객체를 생성하지 않고 클래스 이름을 통해서 접근할 수 있다.
```java
public class Car {
    public static String compay = "hyundai";

    public Car() {
    }
}

System.out.println(Car.compay); // hyundai
```

## 🍉static method
> static method를 사용하면, 객체를 생성하지 않고 그 메소드를 호출할 수 있다.
```java
public class Car {
    public static String compay = "hyundai";

    public static void print() {
		System.out.println(compay);
    }
}

System.out.println(Car.print()); // hyundai
```

## 🍇static class
> static 키워드를 이용하여 class를 선언하면, 상위 클래스와 분리 한다.
- static으로 선언한 하위 클래스를 외부에서 직접 객체를 생성할 수 있다.
```java
public class Car {
    public int price = 20000;

    public Car() {
    }

    public static class Bumper {
        public Bumper() {
            // price = 2000; // compile error.
        }
    }
}

Car.Bumper bp = new Car.Bumper();
```