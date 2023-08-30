## 싱글톤 ___Singleton___ (Extra : static)


### static

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
## 장점
#### 1. 리소스 절약
- 하나의 인스턴스만을 생성하기 위해 사용합니다. 여러개의 인스턴스가 필요하지 않는 경우 생성합니다. 하나의 인스턴스를 여러곳에서 사용 한다면 리소스를 절약할 수 있습니다.

#### 2. 데이터 공유
- 위에서 언급한 것처럼 하나의 인스턴스만이 존재하기 때문에, 그 인스턴스를 통해 데이터를 쉽게 공유할 수 있습니다. 데이터베이스 연결이나 네트워크 소켓처럼 여러 곳에서 공유되어야 하는 리소스를 관리할 때 유용하게 쓰일 수 있습니다.

#### 3. 중복 방지
- 여러 번 인스턴스를 생성한다면 불필요한 인스턴스의 중복생성이 발생합니다. 싱글톤을 사용하면 이런 중복을 피할 수 있고, 이로 인해 프로그램의 안정성이나 효율을 향상시킬 수 있습니다.

#### 4. 전역 상태 관리
- 글로벌(전역) 변수를 사용하는 것보다 싱글톤을 사용하면 전역 상태를 좀 더 안전하고 효율적으로 관리할 수 있습니다.

#### 5. 제어된 접근
- 싱글톤 패턴을 사용하면 인스턴스에 대한 접근을 제어할 수 있습니다.

---

#### 클래스가 로드될 때 즉시 초기화.
- ___Eager Initialization___

```
public class Singleton {
  private static final Singleton instance = new Singleton();

  private Singleton() {
    // private constructor
  }

  public static Singleton getInstance() {
    return instance;
  }
}
```

---

#### 인스턴스가 필요할 때까지 생성을 미루는 생성방법
- ___Lazy Initialization___

```
public class Singleton {
  private static Singleton instance = null;

  private Singleton() {
    // private constructor
  }

  public static Singleton getInstance() {
    if (instance == null) {
      instance = new Singleton();
    }
    return instance;
  }
}
```

---

### __※ 정리__
- Singleton 패턴은 언제 어디서든 편하게 호출하여 데이터를 쉽게 공유하고 리소스를 절약할 수 있기에 자주사용되는 디자인 패턴중 하나입니다.


---
<!--목차 & 다음으로 페이지 이동-->
[목차](https://github.com/Devcurve/Java/blob/main/README.md)<br>
[이전 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/class.md)<br>
[다음 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/inheritance.md
