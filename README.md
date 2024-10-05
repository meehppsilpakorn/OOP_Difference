---
cover: .gitbook/assets/New Project (9).png
coverY: 0
layout:
  cover:
    visible: true
    size: full
  title:
    visible: true
  description:
    visible: false
  tableOfContents:
    visible: true
  outline:
    visible: true
  pagination:
    visible: true
---

# OOP Programming

OOP (Object-Oriented Programming) คือ การเขียนโปรแกรมในรูปแบบวัตถุ(Object) ซึ่งภายในวัตถุจะประกอบไปด้วย ข้อมูล(Data) และ การกระทำ(Action) หรือก็คือ เขียนโปรแกรมให้เสมือนกับวัตถุในโลกจริง&#x20;

<figure><img src=".gitbook/assets/Pro (1).png" alt=""><figcaption><p>Difference of Procedural Programming vs. Object-Oriented Programming</p></figcaption></figure>

### แนวคิด OOP

OOP จะมีแนวคิดที่ต่างจาก POP (Procedural Programming) ซึ่งมีการสืบทอด(Inheritance), การมีได้หลายรูปแบบ(Polymorphism) และ การห่อหุ่ม(Encapsulation)&#x20;

<table data-full-width="false"><thead><tr><th>Feature</th><th>POP(Procedural)</th><th>OOP(Object-Oriented)</th></tr></thead><tbody><tr><td>Focus</td><td>Procedures (functions)</td><td>Objects (data + behavior)</td></tr><tr><td>Program Structure</td><td>Sequence of functions</td><td>Objects interacting with each other</td></tr><tr><td>Data Organization</td><td>Global/local variables, function arguments</td><td>Encapsulated within objects</td></tr><tr><td>Code Reusability</td><td>Limited, prone to duplication</td><td>High through inheritance and polymorphism</td></tr><tr><td>Maintainability</td><td>Challenging for large projects</td><td>Improved due to encapsulation and inheritance</td></tr><tr><td>Suitability</td><td>Simple tasks, smaller projects, education</td><td>Complex projects, code reusability, real-world modeling</td></tr><tr><td>Example Languages</td><td>C, FORTRAN, Pascal</td><td>C++, Java, Python, C#</td></tr></tbody></table>

### ความแตกต่างของ OOP ในแต่ละภาษา&#x20;

ในที่นี้จะกล่าวถึง 3 ภาษาโปรแกรม นั้นคือ Java, C++, Python

#### JAVA

* **Pure OOP** : เนื่องด้วยทุกอย่างในภาษา Java ล้วนถูกมองว่าเป็นวัตถุ แม้กระทั้งชนิดข้อมูลพื้นฐาน(Primitive Data Types) ก็ถูกจัดเป็นวัตถุ เช่น `Integer` `Double`
* **Syntax and Structure** : ภาษา Java เป็นภาษาที่เข้มงวดในด้านชนิดข้อมูล statically-typed system ซึ่งต้องมีการประกาศ(Declare) ตั้งแต่ Class รวมถึง attribute, method ต้องประกาศชนิดข้อมูลทั้งสิ้น

```java
class Animal{ //Class declaration
    String name; //attribute declaration
    int weight;
    int height;
    
    Animal (){ //method declaration
        //...
    }
}
```

* **Encapsulation** : มีการห่อหุ้มด้วยการกำหนดการเข้าถึงข้อมูล(Access Modifier) -> `public`, `private`, `protected`, `default` และถ้าต้องการเข้าถึงจะต้องกำหนด getter, setter แทน

```java
class Animal{ 
    private String name; // private -> access modifier
    private int weight;
    private int height;
    
    public Animal (){ 
        //...
    }
}
```

* **Inheritance and Polymorphism** : สนับสนุนการสืบทอดแบบเดี่ยว โดยใช้ `extends` และสามารถสืบทอดคุณสมบัติจากคลาสพ่อ(Parents Class) มากกว่าหนึ่งคลาส โดยใช้`implements`

```java
class Cat extends Animal{ 
    //...
}
```

* **Abstraction** : คลาสนามธรรม ซึ่งใช้สำหรับออกแบบรูปแบบโปรแกรม(Design Patterns)  เพื่อแสดงลำดับขั้นในโครงสร้าง(structured hierarchies) ซึ่งใช้ทั้ง คลาสนามธรมม(Abstract Class), อินเตอร์เฟส(Interface)&#x20;

```java
abstract class ZooKeeper{ 
    //...
}
```

* **Memory Management** : มีการจัดการขยะด้วย Garbage Collector เมื่อมีข้อมูลที่ไม่สามารถเข้าถึงได้เกิดขึ้น
* **Use Case** : มักใช้ในโปรเจคขนาดใหญ่, Android Application, web services

#### Python

* **Dynamic Typing** : ภาษา Python เป็น dynamically typed language หมายถึง ไม่จำเป็นต้องกำหนดชนิดข้อมูลขณะประกาศตัวแปร ซึ่งถ้าไม่ระวังอาจส่งผลให้เกิด error ในขณะ  runtime ได้
* **Syntax and Structure** : ทุกอย่างเป็น object เหมือนกับ Java, ไวยากรณ์ในภาษา Python เรียบง่าย และหลากหลายกว่า Java, C++  ทำให้ในบางสถานการณ์ เขียนโค้ดได้สั้นกว่า
* **Encapsulation** : ภาษา Python ไม่ได้ที access modifier เหมือนอย่าง  Java, C++ แต่ใช้ prefix ไว้หน้า attribute เช่น \_attribute เพื่อบ่งบอกว่า attribute นี้ ไม่สามารถเข้าถึงจากภายนอกได้
* **Inheritance and Polymorphism** : สนับสนุนทั้ง single, multiple Inheritance ซึ่ง Python แข็งแกร่งในด้าน Polymorphism โดยใช้วิธี Duck typing เนื่องจากไม่ได้มีการเช็คชนิดข้อมูลที่เข้มงวด จึ่งสามารถเขียนดังตัวอย่าง

```python
def animal_sound(animal):
    print(animal.speak())

# Define multiple classes with similar method names
class Dog:
    def speak(self):
        return "Woof!"

class Cat:
    def speak(self):
        return "Meow!"

class Duck:
    def speak(self):
        return "Quack!"

dog = Dog()
cat = Cat()
duck = Duck()

# All instances can be passed to the same function
animal_sound(dog)   # Output: Woof!
animal_sound(cat)   # Output: Meow!
animal_sound(duck)  # Output: Quack!
```

* **Abstraction** : สนับสนุนคลาสนามธรรมผ่าน `abc` module (Abstract Base Class)

```python
from abc import ABC, abstractmethod

# Abstract Base Class
class Shape(ABC):
    # Abstract method that must be implemented by subclasses
    @abstractmethod
    def area(self):
        pass
    
    @abstractmethod
    def perimeter(self):
        pass

# Concrete Class inheriting from the abstract class Shape
class Rectangle(Shape):
    def __init__(self, width, height):
        self.width = width
        self.height = height
    
    # Implementing the abstract methods
    def area(self):
        return self.width * self.height
    
    def perimeter(self):
        return 2 * (self.width + self.height)

# Another Concrete Class inheriting from the abstract class Shape
class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    
    # Implementing the abstract methods
    def area(self):
        return 3.1416 * (self.radius ** 2)
    
    def perimeter(self):
        return 2 * 3.1416 * self.radius
```

* **Memory Management** : จัดการหน่วยความจำด้วย garbage collector เหมือนกับ Java แต่สามารถทำได้หลากหลายกว่าด้วย `del` , `None`

```python
a = [1, 2, 3]  # Reference count is 1

b = a          # Reference count increases to 2 (b refers to the same object)

del a          # Reference count decreases to 1 (only b refers to the object)

b = None       # Reference count decreases to 0 (no more references to the object)
# The list [1, 2, 3] is now garbage-collected.
```

* **Use Case** : ส่วนใหญ่ใช้ในด้าน computer science, data analysis, machine learning เนื่องจากมี library ที่สนับสนุนงานด้านที่หลากหลายมากกว่า Java, C++

#### C++

* **Hybrid OOP** : C++ เป็นภาษาที่งสามารถทำเป็น POP หรือ OOP ได้ขึ่นอยู่กับนักพัฒนา(developer) ต้องการเขียนในรูปแบบใด
* **Syntax and Structure** : C++ ประกาศชนิดข้อมูลแบบเดียวกับ Java นั้นคือ statically typed และยังมีไวยากรณ์ซับซ้อนที่มากกว่าทั้งใน Java, Python
* **Encapsulation** : ห่อหุ้มวัตถุเช่นเดียวกับ Java รวมถึง access modifier
* **Inheritance and Polymorphism** : สนับสนุนการสืบทอดแบบเดี่ยว(single Inheritance) และสามารถสืบทอดคุณสมบัติจากคลาสพ่อ มากกว่าหนึ่งคลาส (multiple Inheritance) แต่จะพบปัญหา "diamond problem" ซึ่งแก้ไขได้ด้วย virtual inheritance รวมถึงการมีหลายรูปแบบ(Polymorphic) โดยใช้ virtual function
* **Abstraction** : สนับสนุนทั้งคลาสนามธรรม และ pure virtual function
* **Manual Memory Management** : C++ ไม่ได้มี garbage collector เหมือนอย่าง Java, Python ต้องให้นักพัฒนาเรียกใช้คำสั่งขึ้นมาเอง เช่น `new`, `delete`, etc. ซึ่งมีส่งผลในด้านดีของประสิทธิภาพมากกว่า แต่ต้องใช้อย่างระมัดระวัง
* **Performance** : ในด้านประสิทธิภาพ (Performance) C++ อยู่ในระดับที่สูง high performance ใช้กับงานที่มุ่งเน้นประสิทธิภาพเป็นหลัก เช่น game development, real-time systems, และ embedded systems.
* **ตัวอย่างโค้ด**

```cpp
#include <iostream>
#include <cmath> 

// Abstract Class 
class Shape {
protected:
    std::string name;
public:
    Shape(const std::string& n) : name(n) {}
    
    // Pure virtual function 
    virtual double area() const = 0;
    
    // Virtual function สำหรับแสดงข้อมูล Shape
    virtual void display() const {
        std::cout << "Shape: " << name << std::endl;
    }
    
    // Virtual Destructor สำหรับ destuctor
    virtual ~Shape() {}
};

// Inheritance
class Circle : public Shape {
private:
    double radius;  // Encapsulation 
    
public:
    Circle(double r) : Shape("Circle"), radius(r) {}
    
    // Overriding method (Polymorphism)
    double area() const override {
        return M_PI * radius * radius;
    }

    void display() const override {
        std::cout << "Shape: " << name << ", Radius: " << radius << ", Area: " << area() << std::endl;
    }
};

//(Inheritance)
class Rectangle : public Shape {
private:
    double width, height;  // Encapsulation
    
public:
    Rectangle(double w, double h) : Shape("Rectangle"), width(w), height(h) {}

    double area() const override {
        return width * height;
    }
    
    // Overriding display method
    void display() const override {
        std::cout << "Shape: " << name << ", Width: " << width << ", Height: " << height << ", Area: " << area() << std::endl;
    }
};

void printShapeInfo(const Shape& shape) {
    shape.display();
}

int main() {
    Circle circle(5.0);  
    Rectangle rectangle(4.0, 6.0);  
    
    //polymorphism สำหรับแสดงข้อมูล
    printShapeInfo(circle);     // Calls Circle's display method
    printShapeInfo(rectangle);  // Calls Rectangle's display method

    return 0;
}
```

### สรุปความแตกต่างของ Java, Python, C++

ที่กล่าวมาข้างต้นสามารถสรุปในรูปแบบตารางได้ดังนี้

| Feature                  | Java                                | Python                        | C++                                   |
| ------------------------ | ----------------------------------- | ----------------------------- | ------------------------------------- |
| **Typing**               | Statically typed                    | Dynamically typed             | Statically typed                      |
| **Memory Management**    | Automatic (Garbage Collected)       | Automatic (Garbage Collected) | Manual (User controlled)              |
| **Multiple Inheritance** | Through interfaces                  | Directly supported            | Directly supported                    |
| **Syntax**               | Verbose and structured              | Simple and flexible           | Complex and detailed                  |
| **Encapsulation**        | Strict                              | Convention-based              | Strict                                |
| **Speed**                | Slower than C++, faster than Python | Slower than Java and C++      | Fastest                               |
| **Use Case**             | Enterprise, web apps, Android       | Data science, scripting, AI   | Systems, games, high-performance apps |

เห็นได้ว่าแต่ละภาษาโปรแกรมล้วนมีข้อแตกต่าง และเหมาะสมกับงานในตัวเอง นักพัฒนาจำเป็นจะต้องเลือกภาษาให้เหมาะสมกับงานที่ต้องการพัฒนา ซึ่งส่งผลทั้งด้านประสิทธิภาพ และ การแก้ปัญหา
