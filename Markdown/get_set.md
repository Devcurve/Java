## getter & setter


```
public class User {
  private String userName;    // 아이디
  private String password;    // 비밀번호
}
```

- ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼ ▼

```
public class User {
  private String userName;    // 아이디
  private String password;    // 비밀번호

  public String getUserName() { return userName; }
  public void setUserName(String userName) { this.userName = userName; }

  public String getPassword() { return password; }
  public void setPassword(String password) { this.password = password; }
}
```


- `getter`는 값을 참조하기 위해 사용.
- `setter`는 값을 변겅하기 위해 사용.

---
#### getter & setter 사용하는 이유.

>- `캡슐화`<br> 클래스 내부에 있는 데이터를 외부에서 직접 접근하지 못하게 막고, 메서드를 통해서만 접근하도록 하면 무분별한 데이터 값 변경을 방지할 수 있습니다.
- `유효성 검사`<br>setter 메서드에서 데이터의 유효성을 검사할 수 있어습니다. 예를 들면, 나이가 0 이하면 저장하지 않는 등의 로직을 추가할 수 있습니다.

```
public void setAge(int age) {
  if (age > 0) {
    this.age = age;
  }
}
```
>- `가독성과 유지보수`<br>
메서드를 통해 접근하면 어떤 작업을 하는지 메서드 이름만 봐도 이해하기 쉽고, 나중에 내부 로직이 바뀌더라도 메서드 이름은 그대로니까 유지보수하기도 쉬워집니다.
- `추가적인 로직`<br>
getter나 setter에서 추가적인 로직을 넣을 수 있습니다. 값이 변경될 때마다 로깅을 하거나, 다른 필드의 값을 함께 업데이트 할 수 있습니다.
- `API 안정성`<br>
클래스의 내부 구현이 바뀌더라도 getter와 setter의 시그니처는 그대로 유지할 수 있어습니다. 이렇게 되면 해당 클래스를 사용하는 다른 코드를 변경하지 않고도 클래스 내부의 구현을 자유롭게 바꿀 수 있어습니다.
- `다형성 활용`<br>
getter와 setter를 오버라이딩해서 자식 클래스에서 다른 동작을 하게 할 수도 있어습니다. 이런식으로 다형성을 활용할 수 있습니다.

---
<!--목차 & 다음으로 페이지 이동-->
[목차](https://github.com/Devcurve/Java/blob/main/README.md)<br>
[이전 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/constructor.md)<br>
<!--[다음 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/get_set.mㅇ-->
