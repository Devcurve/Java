## 생성자 ___Constructor___
- 생성자는 객체가 생성될 때 자동으로 호출되는 메서드로, 객체의 초기화 작업을 수행합니다.

```
public class Person {
    String name;

    // 생성자
    public Person(String name) {
        this.name = name;
    }
}
```

---
## 복사 생성자 ___Copy Constructor___
- 복사 생성자는 기존 객체의 값을 복사하여 새로운 객체를 생성하는 생성자 입니다.

```
public class Person {
    String name;

    // 생성자
    public Person(String name) {
        this.name = name;
    }

    // 복사 생성자
    public Person(Person person) {
        this.name = person.name;
    }
}
```


## 가비지 컬렉터 ___Garbage Collector___

```
Person person1 = new Person("홍길동");
person1 = null; // person1 객체에 대한 참조를 제거

// 가비지 컬렉터가 person1 객체를 제거할 수 있다.
System.gc(); // 가비지 컬렉터를 명시적으로 호출 (선택 사항)    
```

---
<!--목차 & 다음으로 페이지 이동-->
[목차](https://github.com/Devcurve/Java/blob/main/README.md)<br>
[이전 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/function.md)<br>
<!--[다음 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/constructor.md-->
