
# Static

## ๐static field
> static field๋ฅผ ์ฌ์ฉํ๋ฉด, ๊ฐ์ฒด๋ฅผ ์์ฑํ์ง ์๊ณ  ํด๋์ค ์ด๋ฆ์ ํตํด์ ์ ๊ทผํ  ์ ์๋ค.
```java
public class Car {
    public static String compay = "hyundai";

    public Car() {
    }
}

System.out.println(Car.compay); // hyundai
```

## ๐static method
> static method๋ฅผ ์ฌ์ฉํ๋ฉด, ๊ฐ์ฒด๋ฅผ ์์ฑํ์ง ์๊ณ  ๊ทธ ๋ฉ์๋๋ฅผ ํธ์ถํ  ์ ์๋ค.
```java
public class Car {
    public static String compay = "hyundai";

    public static void print() {
		System.out.println(compay);
    }
}

System.out.println(Car.print()); // hyundai
```

## ๐static class
> static ํค์๋๋ฅผ ์ด์ฉํ์ฌ class๋ฅผ ์ ์ธํ๋ฉด, ์์ ํด๋์ค์ ๋ถ๋ฆฌ ํ๋ค.
- static์ผ๋ก ์ ์ธํ ํ์ ํด๋์ค๋ฅผ ์ธ๋ถ์์ ์ง์  ๊ฐ์ฒด๋ฅผ ์์ฑํ  ์ ์๋ค.
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