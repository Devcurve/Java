## class 사용 예제

```
// 동물 클래스
class Animal {
    // 속성: 이름, 나이
    private String name;
    private int age;

    // 생성자
    public Animal(String name, int age) {
        this.name = name;
        this.age = age;
    }

    // getter & setter
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }

    public int getAge() {
        return age;
    }
    public void setAge(int age) {
        this.age = age;
    }

    // 메서드: 동물 소리
    public void makeSound() {
        System.out.println("동물이 소리를 냅니다.");
    }
}

public class Main {
    public static void main(String[] args) {
        // 동물 객체 생성
        Animal animal = new Animal("멍멍이", 3);

        // 동물 이름 출력
        System.out.println(animal.getName());

        // 동물 소리 출력
        animal.makeSound();
    }
}
```

---

```
// 계산기 클래스
class Calculator {
    // 속성: 현재 값
    private double currentValue;

    // 생성자
    public Calculator() {
        this.currentValue = 0.0;
    }

    // getter & setter
    public double getCurrentValue() {
        return currentValue;
    }
    public void setCurrentValue(double currentValue) {
        this.currentValue = currentValue;
    }

    // 메서드: 더하기
    public void add(double value) {
        this.currentValue += value;
    }

    // 메서드: 빼기
    public void subtract(double value) {
        this.currentValue -= value;
    }
}

public class Main {
    public static void main(String[] args) {
        // 계산기 객체 생성
        Calculator calc = new Calculator();

        // 10 더하기
        calc.add(10);
        System.out.println(calc.getCurrentValue());

        // 5 빼기
        calc.subtract(5);
        System.out.println(calc.getCurrentValue());
    }
}
```

---

```
// 학생 클래스
class Student {
    // 속성: 이름, 학년
    private String name;
    private int grade;

    // 생성자
    public Student(String name, int grade) {
        this.name = name;
        this.grade = grade;
    }

    // getter & setter
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }

    public int getGrade() {
        return grade;
    }
    public void setGrade(int grade) {
        this.grade = grade;
    }

    // 메서드: 자기소개
    public void introduce() {
        System.out.println("안녕, 나는 " + name + ", " + grade + "학년이야.");
    }
}

public class Main {
    public static void main(String[] args) {
        // 학생 객체 생성
        Student student = new Student("지민", 5);

        // 자기소개
        student.introduce();
    }
}
```

---

```
// 차 클래스
class Car {
    // 속성: 브랜드, 연식
    private String brand;
    private int year;

    // 생성자
    public Car(String brand, int year) {
        this.brand = brand;
        this.year = year;
    }

    // getter & setter
    public String getBrand() {
        return brand;
    }
    public void setBrand(String brand) {
        this.brand = brand;
    }

    public int getYear() {
        return year;
    }
    public void setYear(int year) {
        this.year = year;
    }

    // 메서드: 차를 운전한다
    public void drive() {
        System.out.println(brand + " 차를 운전합니다.");
    }
}

public class Main {
    public static void main(String[] args) {
        // 차 객체 생성
        Car car = new Car("포르쉐", 2020);

        // 차를 운전한다
        car.drive();
    }
}
```

---

```
// 책 클래스
class Book {
    // 속성: 제목, 저자
    private String title;
    private String author;

    // 생성자
    public Book(String title, String author) {
        this.title = title;
        this.author = author;
    }

    // getter & setter
    public String getTitle() {
        return title;
    }
    public void setTitle(String title) {
        this.title = title;
    }

    public String getAuthor() {
        return author;
    }
    public void setAuthor(String author) {
        this.author = author;
    }

    // 메서드: 책 정보를 출력한다
    public void showInfo() {
        System.out.println("제목: " + title + ", 저자: " + author);
    }
}

public class Main {
    public static void main(String[] args) {
        // 책 객체 생성
        Book book = new Book("해리포터", "J.K. 롤링");

        // 책 정보 출력
        book.showInfo();
    }
}
```

---

```
// 과일 클래스
class Fruit {
    // 속성: 이름, 색깔
    private String name;
    private String color;

    // 생성자
    public Fruit(String name, String color) {
        this.name = name;
        this.color = color;
    }

    // getter & setter
    public String getName() {
        return name;
    }
    public void setName(String name) {
        this.name = name;
    }

    public String getColor() {
        return color;
    }
    public void setColor(String color) {
        this.color = color;
    }

    // 메서드: 과일 정보 출력
    public void showInfo() {
        System.out.println("이 과일은 " + name + "이고, 색깔은 " + color + "야.");
    }
}

public class Main {
    public static void main(String[] args) {
        // 과일 객체 생성
        Fruit fruit = new Fruit("사과", "빨간색");

        // 과일 정보 출력
        fruit.showInfo();
    }
}
```

---

```
// 음악 클래스
class Music {
    // 속성: 제목, 가수
    private String title;
    private String singer;

    // 생성자
    public Music(String title, String singer) {
        this.title = title;
        this.singer = singer;
    }

    // getter & setter
    public String getTitle() {
        return title;
    }
    public void setTitle(String title) {
        this.title = title;
    }

    public String getSinger() {
        return singer;
    }
    public void setSinger(String singer) {
        this.singer = singer;
    }

    // 메서드: 음악을 재생한다
    public void play() {
        System.out.println(title + "을(를) 재생합니다.");
    }
}

public class Main {
    public static void main(String[] args) {
        // 음악 객체 생성
        Music music = new Music("Dynamite", "BTS");

        // 음악을 재생한다
        music.play();
    }
}
```

---

```
// 펜 클래스
class Pen {
    // 속성: 색깔, 두께
    private String color;
    private double thickness;

    // 생성자
    public Pen(String color, double thickness) {
        this.color = color;
        this.thickness = thickness;
    }

    // getter & setter
    public String getColor() {
        return color;
    }
    public void setColor(String color) {
        this.color = color;
    }

    public double getThickness() {
        return thickness;
    }
    public void setThickness(double thickness) {
        this.thickness = thickness;
    }

    // 메서드: 글씨를 쓴다
    public void write() {
        System.out.println(color + " 색으로 글씨를 씁니다.");
    }
}

public class Main {
    public static void main(String[] args) {
        // 펜 객체 생성
        Pen pen = new Pen("파란색", 0.5);

        // 글씨를 쓴다
        pen.write();
    }
}
```

---

```
// 피자 클래스
class Pizza {
    // 속성: 크기, 토핑
    private String size;
    private String topping;

    // 생성자
    public Pizza(String size, String topping) {
        this.size = size;
        this.topping = topping;
    }

    // getter & setter
    public String getSize() {
        return size;
    }
    public void setSize(String size) {
        this.size = size;
    }

    public String getTopping() {
        return topping;
    }
    public void setTopping(String topping) {
        this.topping = topping;
    }

    // 메서드: 피자를 만든다
    public void make() {
        System.out.println(size + " 크기의 " + topping + " 토핑 피자를 만듭니다.");
    }
}

public class Main {
    public static void main(String[] args) {
        // 피자 객체 생성
        Pizza pizza = new Pizza("Large", "치즈");

        // 피자를 만든다
        pizza.make();
    }
}

```

---

```
// 텔레비전 클래스
class Television {
    // 속성: 브랜드, 크기
    private String brand;
    private int size;

    // 생성자
    public Television(String brand, int size) {
        this.brand = brand;
        this.size = size;
    }

    // getter & setter
    public String getBrand() {
        return brand;
    }
    public void setBrand(String brand) {
        this.brand = brand;
    }

    public int getSize() {
        return size;
    }
    public void setSize(int size) {
        this.size = size;
    }

    // 메서드: TV를 켠다
    public void turnOn() {
        System.out.println(brand + " 텔레비전을 켭니다.");
    }
}

public class Main {
    public static void main(String[] args) {
        // 텔레비전 객체 생성
        Television tv = new Television("삼성", 55);

        // TV를 켠다
        tv.turnOn();
    }
}

```

---
---
<!--목차 & 다음으로 페이지 이동-->
[목차](https://github.com/Devcurve/Java/blob/main/README.md)<br>
[이전 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/get_set.md)<br>
[다음 페이지](https://github.com/Devcurve/Java/blob/main/Markdown/singleton.md)
