

# String

## 🍺method

**해당 인덱스에 위치한 문자 반환**
```java
char ch = s.charAt(5);
```
<hr />

**문자열 더하기**
```java
s = s.concat(s2);
```
<hr />

**소문자로 바꾸기**
```java
s.toLowerCase();
```
<hr />

**대문자로 바꾸기**
```java
s.toUpperCase();
```
<hr />

**대소문자 구분없이 비교**
```java
s.equalsIgnoreCase(s2);
```
<hr />

**부분 문자열 출력**
```java
s = s.substring(3); // 3번 인덱스부터 끝까지 출력
s = s.substring(5,7); // 시작값 포함, 끝값 미포함
```
<hr />


**문자열 바꾸기**
```java
s = s.replace("EO", "korea");
```
<hr />

**구분자로 문자열 배열 만들기**
```java
s = "123-4567-8952";
String[] strArr = s.split("-");
```
<hr />

**문자열을 char 배열로 만들기**
```java
char[] charArr = s.toCharArray();
```
<hr />

**공백 문자 지우기**
```java
s = s.trim();
```
<hr />

**문자열 주소 반환** 
```java
s.hashCode();
```


## 🍹String.split() vs StringTokenizer()


- 구분자 사이에 데이터가 없는 경우, split만 공백 데이터를 반환한다.
```java
String str = "apple,banana,,kiwi";
str.split(",") // "apple" "bababa" "" "kiwi"  4개
st = StringTokenizer(str, ",");  // "apple" "bababa" "kiwi" : 3개
st.countTokens() 
 ```



