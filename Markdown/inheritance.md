## 상속 ___(inheritance)___

#### 상속이란?
- 상속(inheritance)은 하나의 클래스가 다른 클래스의 변수나 메서드를 물려받는 것을 의미합니다. 이렇게 하면, 같은 기능이나 변수를 여러 클래스에서 재사용할 수 있습니다. 이렇게 작성한다면 코드를 효율적으로 작성할 수 있어 많이 활용되고 있습니다.

#### Java에서의 상속
- Java에서 상속을 사용하려면 extends 키워드를 사용해야 합니다. 만약 Animal이라는 클래스가 있고, Dog이라는 클래스가 그 기능을 물려받아야 한다면 아래와 예제와 같이 작성해볼 수 있습니다.

```
class Animal {
    public void makeSound() {
        System.out.println("동물이 소리를 냅니다.");
    }
}

class Dog extends Animal {
    // 여기서는 Animal 클래스의 makeSound 메서드를 그대로 사용할 수 있습니다.
}
```

- ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼

```
class Animal {
    public void makeSound() {
        System.out.println("동물이 소리를 냅니다.");
    }
}

class Dog extends Animal {
  // 클래스를 비워두겠습니다.
}

public class Main {
    public static void main(String[] args) {
        // Animal 객체 생성 : Animal 클래스에서 함수를 호출 합니다.
        Animal animal = new Animal();
        animal.makeSound();  // 출력: "동물이 소리를 냅니다."

        // Dog 객체 생성 : Dog 클래스에서 함수를 호출 합니다.
        Dog dog = new Dog();
        dog.makeSound();  // 호출이 가능합니다.
    }
}
```


#### 부모 클래스와 자식 클래스
- 상속에서는 두 가지 주요 클래스 유형이 있습니다.

>부모 클래스 (Parent Class): 기능을 물려주는 클래스. 위 예제에서는 Animal.<br>
자식 클래스 (Child Class): 기능을 물려받는 클래스. 위 예제에서는 Dog.


#### 메서드 오버라이딩 (Method Overriding)
자식 클래스는 부모 클래스의 메서드를 그대로 사용할 수도 있고, 필요에 따라 그 메서드를 자신의 클래스에 맞게 변경할 수도 있습니다. 이것을 `오버라이딩` 이라고 합니다.

```
class Animal {
    public void makeSound() {
        System.out.println("동물이 소리를 냅니다.");
    }
}

class Dog extends Animal {
    // 부모 클래스의 makeSound 메서드를 오버라이딩
    public void makeSound() {
        System.out.println("멍멍!");
    }
}

class Cat extends Animal {
    // 부모 클래스의 makeSound 메서드를 오버라이딩
    public void makeSound() {
        System.out.println("야옹!");
    }
}

public class Main {
    public static void main(String[] args) {
        // Animal 객체 생성
        Animal myAnimal = new Animal();
        myAnimal.makeSound();  // 출력: "동물이 소리를 냅니다."

        // Dog 객체 생성
        Dog myDog = new Dog();
        myDog.makeSound();  // 출력: "멍멍!"

        // Cat 객체 생성
        Cat myCat = new Cat();
        myCat.makeSound();  // 출력: "야옹!"
    }
}
```

- `protected` : 상속의 경우에서는 `public`과 같은 형태로 사용 가능하지만 상속이 아닌 경우에는 `private`와 같다.
- 자식 클래스는 부모 클래스의 모든 public과 protected 멤버(변수, 메서드)를 물려받지만, private 멤버는 물려받을 수 없습니다.


```
class Animal {
    protected String say;

    public void makeSound() {
        System.out.println("동물이 소리를 냅니다.");
    }
}

class Dog extends Animal {
    Dog(){
      say = "멍멍!";
    }

    // 부모 클래스의 makeSound 메서드를 오버라이딩
    public void makeSound() {
        System.out.println(say);
    }
}

class Cat extends Animal {
    Cat(){
      say = "야옹!";
    }

    // 부모 클래스의 makeSound 메서드를 오버라이딩
    public void makeSound() {
        System.out.println(say);
    }
}

public class Main {
    public static void main(String[] args) {
        // Animal 객체 생성
        Animal myAnimal = new Animal();
        myAnimal.makeSound();  // 출력: "동물이 소리를 냅니다."

        // Dog 객체 생성
        Dog myDog = new Dog();
        myDog.makeSound();  // 출력: "멍멍!"

        // Cat 객체 생성
        Cat myCat = new Cat();
        myCat.makeSound();  // 출력: "야옹!"
    }
}
```

___예제___


```
class Animal {
    public void makeSound() {
        System.out.println("동물이 소리를 냅니다.");
    }
}

class Dog extends Animal {
    // 부모 클래스의 makeSound 메서드를 오버라이딩
    public void makeSound() {
        System.out.println("멍멍!");
    }
}

class Cat extends Animal {
    // 부모 클래스의 makeSound 메서드를 오버라이딩
    public void makeSound() {
        System.out.println("야옹!");
    }
}

public class Main {
    public static void main(String[] args) {
        // Animal 객체 생성
        Animal myAnimal = new Animal();
        myAnimal.makeSound();  // 출력: "동물이 소리를 냅니다."

        // Dog 객체 생성
        Dog myDog = new Dog();
        myDog.makeSound();  // 출력: "멍멍!"

        // Cat 객체 생성
        Cat myCat = new Cat();
        myCat.makeSound();  // 출력: "야옹!"
    }
}

```

---

## 추상화 ___abstract___

### 순수 가상함수
- `순수 가상 함수`는 선언만 있고 구현이 없는 함수를 의미합니다. `순수 가상 함수`가 있는 클래스를 `추상 클래스(abstract class)`라고 하며, 이 클래스를 상속받는 하위 클래스에서는 상위 클래스에서 선언한 `순수 가상 함수`를 반드시 구현해야 합니다.

> 예
```
public abstract class Animal {
    public abstract void makeSound();
}
public class Dog extends Animal {
    public void makeSound() {
        System.out.println("왈왈!");
    }
}
```


___예제___

```
public abstract class Animal {
    // 순수 가상 함수
    public abstract void makeSound();
}

public class Dog extends Animal {
    // Animal 클래스에서 정의한 순수 가상 함수 makeSound를 구현
    public void makeSound() {
        System.out.println("왈왈!");
    }
}

public class Cat extends Animal {
    // Animal 클래스에서 정의한 순수 가상 함수 makeSound를 구현
    public void makeSound() {
        System.out.println("냐옹~");
    }
}

public class Main {
    public static void main(String[] args) {
      Animal myDog = new Dog();
      myDog.makeSound();

      Animal myCat = new Dog();
      myCat.makeSound();
    }
}
```


---
<!--목차 & 다음으로 페이지 이동-->
[목차](https://github.com/Devcurve/Java/blob/main/README.md)<br>
[이전 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/Singleton.md)<br>
<!--[다음 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/inheritance.md-->
