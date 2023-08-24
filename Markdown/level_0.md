## 출력

#### "안녕, 자바!"를 출력하는 프로그램을 작성해 보세요.

```
출력
>> 안녕, 자바!
```

---

#### 네 개의 정수 10, 20, 30, 40을 한 줄에 출력해보세요.

```
int a = 10;
int b = 20;
int c = 30;
int d = 40;

출력
>>  10, 20, 30, 40
```

---

#### 자신의 이름과 나이를 출력하는 프로그램을 만들어보세요.

```
예:
String name = "홍길동"
int age = 24

출력
>> 홍길동, 24
```

---

#### 두 개의 `실수`를 더한 결과를 출력해보세요.

```
예 3.14, 3.14

출력
>>  6.28
```

---

## if문의 활용

#### 정수를 입력받아 양수인지 음수인지 판별해 보세요.
- `import java.util.Scanner;` 포함.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 입력
        System.out.print("정수를 입력하세요: ");
        int number = scanner.nextInt();

        // ** 이 부분에 if문을 활용한 비교문을 작성합니다.




        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```

---

#### 세 개의 숫자 중 가장 큰 숫자를 찾아 출력해 보세요.
- `import java.util.Scanner;` 포함.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 입력
        System.out.print("첫 번째 숫자를 입력하세요: ");
        int num1 = scanner.nextInt();

        System.out.print("두 번째 숫자를 입력하세요: ");
        int num2 = scanner.nextInt();

        System.out.print("세 번째 숫자를 입력하세요: ");
        int num3 = scanner.nextInt();


        // ** 이 부분에 if문을 활용한 비교문을 작성합니다.




        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```

---

#### 나이를 입력받아 성인인지 미성년자인지 판별해 보세요.
- `import java.util.Scanner;` 포함.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 입력
        System.out.print("나이를 입력하세요: ");
        int age = scanner.nextInt();

        // ** 이 부분에 if문을 활용한 비교문을 작성합니다.




        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```

---

#### 점수를 입력받아 학점을 출력해 보세요.
- `import java.util.Scanner;` 포함.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 입력
        System.out.print("점수를 입력하세요: ");
        int score = scanner.nextInt();

        // ** 이 부분에 if문을 활용한 비교문을 작성합니다.



        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```

---

#### 현재 시간을 받아 오전인지 오후인지 판별해 보세요.
- `import java.util.Scanner;` 포함.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 입력
        System.out.print("현재 시간을 입력하세요(24시간 형식): ");
        int hour = scanner.nextInt();

        // ** 이 부분에 if문을 활용한 비교문을 작성합니다.




        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```

---

## switch문 활용

#### 요일 번호를 입력받아 요일 이름을 출력해 보세요.
- `import java.util.Scanner;` 포함. <br> 1~7사이의 값을 입력받아 각각 월, 화, 수, 목, 금, 토, 일 을 출력합니다.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 입력
        System.out.print("요일 번호를 입력하세요(1-7): ");
        int day = scanner.nextInt();

        // ** 이 부분에 switch문을 활용한 비교문을 작성합니다.




        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```

---

#### '월'을 입력받아 계절을 출력해 보세요.
- `import java.util.Scanner;` 포함. <br> 1~12사이의 값을 입력받아 계절을 출력합니다.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 입력
        System.out.print("'월'을 입력하세요(1-12): ");
        int season = scanner.nextInt();

        // ** 이 부분에 switch문을 활용한 비교문을 작성합니다.




        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```

---

#### 메뉴 번호를 입력받아 음식 이름을 출력해 보세요.
- `import java.util.Scanner;` 포함. <br>[1. 피자, 2. 파스타, 3. 햄버거, 4. 샐러드, 5. 스테이크, 잘못된 메뉴 번호]

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 입력
        System.out.print("메뉴 번호를 입력하세요(1-5): ");
        int menu = scanner.nextInt();

        // ** 이 부분에 switch문을 활용한 비교문을 작성합니다.




        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```

---

#### 성적 등급을 입력받아 평가를 출력해 보세요.
- `import java.util.Scanner;` 포함. <br>[A. 우수, B. 좋음, C. 보통, D. 미흡, F. 불합격, 잘못된 등급]

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 입력
        System.out.print("성적 등급을 입력하세요(A-F): ");
        char grade = scanner.next().charAt(0);

        // ** 이 부분에 switch문을 활용한 비교문을 작성합니다.




        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```


---

## for문 활용

#### 1부터 사용자가 입력한 숫자까지의 합을 구해봐.
- `import java.util.Scanner;` 포함.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 입력
        System.out.print("마지막 값을 입력하세요: ");
        int count = scanner.nextInt();

        // ** 이 부분에 for문을 활용하여 코드를 작성합니다.


        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```

---

#### 2의 거듭제곱을 결과값이 1000을 넘지 않을 때까지 출력해 보세요.

```
public class Main {
    public static void main(String[] args) {

        // 초기값
        int result = 1;

        // ** 이 부분에 for문을 활용하여 코드를 작성합니다.



        // ** 출력
        System.out.println(result);
    }
}
```

---

#### 입력받은 값으로부터 1까지 거꾸로 출력하는 프로그램을 작성해 보세요.
- `import java.util.Scanner;` 포함.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 입력
        System.out.print("마지막 값을 입력하세요: ");
        int count = scanner.nextInt();

        // ** 이 부분에 for문을 활용하여 코드를 작성합니다.


        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```

---

## while문 활용

#### 사용자가 0을 입력할 때까지 숫자를 계속 입력받아 보세요.
- `import java.util.Scanner;` 포함.

```
import java.util.Scanner;

public class Main {
    public static void main(String[] args) {

        // ** 입력받을 객체를 생성 합니다.
        Scanner scanner = new Scanner(System.in);

        // ** 여기부터 while문을 활용하여 코드를 작성합니다.

        // ** 입력
        System.out.print("숫자를 입력하세요 (0을 입력하면 종료): ");
        int number = scanner.nextInt();




        // ** 생성된 객체를 삭제 합니다.
        scanner.close();
    }
}
```

---

#### 사용자가 입력한 숫자의 구구단을 출력해 보세요.
- `import java.util.Scanner;` 포함.

```
```

---



#### 두 숫자의 사칙연산 결과를 출력해 보세요.
- `import java.util.Scanner;` 포함.

```
```

---

#### 세 숫자의 평균을 구해 보세요.
- `import java.util.Scanner;` 포함.

```
```

---

#### 두 숫자를 비교하여 크기를 판별해 보세요.
- `import java.util.Scanner;` 포함.

```
```

---

#### 두 숫자의 나머지를 구해 보세요.
- `import java.util.Scanner;` 포함.

```
```

---

#### 두 숫자의 거듭제곱 값을 구해 보세요.
- `import java.util.Scanner;` 포함.

```
```

---
