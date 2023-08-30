## Static

- `메모리 효율성`: static 변수는 모든 인스턴스에서 공유되므로 메모리를 절약할 수 있습니다.
- `유틸리티 메서드`: 인스턴스화할 필요 없이 기능을 제공하는 유틸리티 클래스를 만들 때 static 메서드를 사용합니다.
- `공유`: 여러 인스턴스가 하나의 데이터를 공유해야 하는 경우에 static 변수를 사용합니다.
- `초기화 블록`: 클래스가 로드될 때 한 번만 수행해야 하는 초기화 작업을 static 블록에서 처리할 수 있습니다.


#### 사용 예제

```
public static int count = 0;
```
- ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼

```
public static void main(String[] args) {
    // 기본 메인 함수
}
```
- ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼

```
public class MyClass {
    public static int[] myArray;

    static {
        myArray = new int[10];
        for (int i = 0; i < 10; i++) {
            myArray[i] = i * i;
        }
    }
}
```
- ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼

```
public class OuterClass {
  public static class InnerClass {
      // ...
  }
}
```


#### 특징
- `생명주기`: static 변수나 메서드는 클래스가 메모리에 로드될 때 초기화되고, 프로그램이 종료될 때까지 유지됩니다.
- `접근 방법`: static 멤버는 클래스 이름으로 직접 접근할 수 있어. 인스턴스를 생성하지 않아도 사용 가능합니다.
- `제약 사항`: static 메서드에서는 static이 아닌 멤버에 직접 접근할 수 없습니다. static 메서드는 인스턴스 생성 없이 호출디기 때문에 인스턴스 변수에 접근할 방법이 없습니다.
- `상속`: static 메서드는 오버라이딩이 허용되지 않습니다. 하위 클래스에서 같은 이름의 static 메서드를 만들면 부모 클래스의 메서드를 사용할 수 없게됩니다.
`Thread Safety`: static 변수는 모든 인스턴스에서 공유되므로 멀티스레드 환경에서는 주의가 필요합니다.

---

### Tip
> static 키워드가 붙은 변수, 메서드, 클래스는 JVM(Java Virtual Machine)에서 클래스가 로드되는 시점에 초기화됩니다.

#### 1. static 변수
static 변수는 클래스가 로드될 때 초기화됩니다. 클래스 로딩은 통상적으로 클래스가 처음 참조되는 시점에 발생합니다. <br>예: `new` 키워드로 인스턴스를 생성 또는 static 메서드의 호출 등..

#### 2. static 메서드
static 메서드도 클래스가 로드되는 시점에 JVM에 등록됩니다. static 메서드는 클래스 이름으로 직접 호출할 수 있고, 인스턴스가 생성되지 않아도 사용 가능합니다.

#### 3. static 클래스 (내부 클래스)
static 클래스는 실제로 내부 클래스에만 static 선언이 가능합니다. static 내부 클래스는 외부 클래스가 로드될 때 함께 로드됩니다. 내부 클래스는 외부 클래스의 인스턴스에 의존하지 않습니다.

#### 4. static 블록
static 블록은 클래스가 로드되는 시점에 실행됩니다. 이 블록은 클래스가 로드될 때 단 한 번만 실행되며, 여러 번 실행되지 않습니다. 이 블록은 주로 static 변수의 복잡한 초기화에 사용됩니다.

---
<!--목차 & 다음으로 페이지 이동-->
[목차](https://github.com/Devcurve/Java/blob/main/README.md)<br>
[이전 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/class.md)<br>
[다음 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/singleton.md)
