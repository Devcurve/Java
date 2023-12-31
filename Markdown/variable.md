## 변수란?
>- 프로그래밍에서 데이터를 저장하는 메모리 공간의 이름입니다.
- 프로그램이 실행되면서 처리해야 할 데이터가 있을 때, 그 데이터를 저장하고 참조할 수 있는 공간이 필요합니다.
- '하나의데이터를 저장할 수 있는 하나의 공간!'으로 기억하면 쉽습니다.

```
int age = 25;
```
>- `int` : 변수는 특정 타입을 가지고 있습니다. 타입은 변수가 저장할 수 있는 데이터의 종류와 크기를 결정합니다. 예를 들면, `int` 타입은 정수를, `double` 타입은 실수를 저장할 수 있습니다.
- `age` : 모든 변수에는 고유한 이름이 있습니다. 이 이름을 통해 프로그램 내에서 해당 변수에 접근할 수 있습니다.
- `25` : 각각의 변수등은 특정 값을 저장할 수 있습니다. 이 값은 프로그램 실행 도중에 변경될 수 있으며, 변수의 타입에 따라 저장할 수 있는 값의 범위가 정해져 있습니다.


---

## 변수 선언 방법

```
// 변수 선언
int number;

// 초기화
number = 10;
```

```
// 변수 선언과 동시에 초기화
int number = 10;
```

```
// 상수 선언과 동시에 값 할당 (상수는 기본적으로 선언 후에는 값을 변경할 수 없기 때문에 선언할 때에만 초기화 가능)
final int number = 10;
```


---

## 의미 있는 이름 사용
- 모든 변수는 그 변수가 어떤 값을 나타내는지 명확하게 표현해야 합니다. 예를 들면, 학생 수를 저장하는 변수일 때 `studentCount` 라는 이름을 지어볼 수 있습니다.

```
int studentCount = 10
```

- __카멜 케이스 사용__: 자바에서는 변수명에 카멜 케이스(camelCase)를 주로 사용합니다. 첫 단어만 소문자로 시작하고, 그 다음 단어의 첫 글자를 대문자로 쓰는 방법입니다. ___예: myVariableName___.

- __짧지만 명확하게__: 너무 길면 코드가 복잡해 보일 수 있습니다. 짧게 하되, 의미를 잃지 않게 하는 게 중요합니다.

- __영문자와 숫자 결합하여 사용__: 변수명은 영문자와 숫자, 밑줄(_)을 사용할 수 있습니다. 하지만 숫자로 시작할 수 없습니다.

- __예약어 피하기__: 자바에는 class, public, static 같은 Java가 사용하고 있는 예약어가 있습니다. 이런 단어는 변수명으로 사용할 수 없습니다.

- __상수는 대문자로__: 상수를 선언할 때는 모든 문자를 대문자로 사용합니다. 단어와 단어 사이에 밑줄을 넣는 걸 관례로 쓰고 있습니다. ___예: MAX_VALUE___.

- __일관성 유지__: 프로젝트나 팀 내에서 변수명을 짓는 규칙을 정하고 그 규칙을 따르는 것도 중요합니다. 일관성 있게 코드를 작성하면 다른 사람이 읽기 쉬워집니다.

---
<!--목차 & 다음으로 페이지 이동-->
[목차](https://github.com/Devcurve/Java/blob/main/README.md)<br>
[다음 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/operator.md)
