## 문자열 ___String___

#### 문자열 생성하기

- 리터럴 상수를 사용한 초기화 방법. String Pool 을 사용한다.

```
String name = "홍길동";
```
<br>

- 동적할당을 사용한 초기화 방법. String 객체를 생성한다.

```
String greeting = new String("안녕하세요!");
```
<br>

#### 문자열 연결하기
- 문자열과 문자열은 서로 `+` 연산자를 사용하여 결합이 가능합니다.

```
String fullName = "홍길동" + "님";
System.out.println(fullName);
```
<br>

#### 문자열 길이 구하기

```
String name = "홍길동";
int length = name.length();
System.out.println(length);
```
<br>

#### 문자열 비교하기
- 문자열이 동일하다면 `true`를 반환한다.

```

String name = "홍길동";
boolean isEqual = name.equals("홍길동");
System.out.println(isEqual);
```
<br>


#### 문자열 부분 추출하기
- java.lang.String.substring(int BeginIndex, int endIndex) 함수 원형 입니다.<br>
문자열 java.lang.String.substring(int BeginIndex, int endIndex)
이 문자열의 하위 문자열인 문자열을 반환합니다. 하위 문자열은 지정된 BeginIndex에서 시작하여 인덱스 endIndex - 1의 문자까지 확장됩니다. 따라서 하위 문자열의 길이는 endIndex-beginIndex입니다.

```
String name = "홍길동";
String part = name.substring(1, 2);
System.out.println(part);
```
<br>

#### 문자열 대소문자 변환하기

```
String name = "Name";
String upper = name.toUpperCase();
String lower = name.toLowerCase();
System.out.println(upper);
System.out.println(lower);
```
<br>

#### 문자열 공백 제거하기

```
String trimmed = "  안녕  !! ".trim();
System.out.println(trimmed);
```
<br>

#### 문자열 치환하기

```
String name = "홍길동";
String replaced = name.replace("홍", "김");
System.out.println(replaced);
```
<br>

#### 문자열 분리하기

```
String[] words = "안녕,하세요,반갑습니다".split(","); // ["안녕", "하세요", "반갑습니다"]
for (int i = 0 ; i < words.length ; ++i ) {
    System.out.println(words[i]);
}
```
<br>

#### 문자열 배열
- String[]은 문자열의 배열을 나타내며, 여러 개의 문자열을 저장할 수 있습니다.

```
String[] names = {"홍길동", "임꺽정", "이몽룡"};
for (int i = 0 ; i < names.length ; ++i ) {
    System.out.println(names[i]);
}
```
<br>

#### 문자열 포맷팅

```
String formatted = String.format("이름: %s, 나이: %d", "홍길동", 30);
System.out.println(formatted);
```
<br>

---
<!--목차 & 다음으로 페이지 이동-->
[목차](https://github.com/Devcurve/Java/blob/main/README.md)<br>
[이전 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/while.md)<br>
[다음 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/array.md)
