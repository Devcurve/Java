## 싱글톤 ___Singleton___

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
[이전 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/static.md)<br>
[다음 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/inheritance.md)
