# 🚀 Python Notes (Beginner → Pro)

> ✨ Clean • Easy • Exam Ready • GitHub Professional

------------------------------------------------------------------------

# 📚 Table of Contents

-   Variables
-   Data Types
-   List
-   Tuple
-   f-String
-   Conditionals
-   Loops
-   Functions
-   Input / Output
-   Operators
-   Type Casting

------------------------------------------------------------------------

# 🧠 1️⃣ Variables

➡️ Variable ek container hota hai jo data store karta hai

### 🔹 Example:

``` python
name = "Jai"
age = 16
```

------------------------------------------------------------------------

# 📦 2️⃣ Data Types

  Type    Meaning
  ------- ------------
  int     Integer
  float   Decimal
  str     Text
  bool    True/False

### 🔹 Example:

``` python
a = 10
b = 3.14
c = "Hello"
d = True
```

------------------------------------------------------------------------

# 📋 3️⃣ List

➡️ Ordered + Mutable collection

### 🔹 Example:

``` python
fruits = ["apple", "banana", "mango"]
```

### 🔹 Important Methods:

``` python
fruits.append("orange")   # Add
fruits.remove("banana")   # Remove
fruits.pop()              # Delete last
```

------------------------------------------------------------------------

# 🔒 4️⃣ Tuple

➡️ Immutable (change nahi hota)

``` python
numbers = (1, 2, 3)
```

------------------------------------------------------------------------

# ⚡ 5️⃣ f-String

➡️ Easy string formatting

``` python
name = "Jai"
age = 16

print(f"My name is {name} and I am {age}")
```

------------------------------------------------------------------------

# 🔀 6️⃣ Conditionals

``` python
age = 18

if age >= 18:
    print("You can vote")
else:
    print("You cannot vote")
```

------------------------------------------------------------------------

# 🔁 7️⃣ Loops

### 🔹 for loop

``` python
for i in range(5):
    print(i)
```

### 🔹 while loop

``` python
i = 1
while i <= 5:
    print(i)
    i += 1
```

------------------------------------------------------------------------

# 🧩 8️⃣ Functions

➡️ Reusable code

``` python
def greet(name):
    print("Hello", name)

greet("Jai")
```

------------------------------------------------------------------------

# ⌨️ 9️⃣ Input / Output

``` python
name = input("Enter your name: ")
print("Hello", name)
```

------------------------------------------------------------------------

# ➕ 🔟 Operators

### Arithmetic:

    +  -  *  /

### Comparison:

    ==  !=  >  <

------------------------------------------------------------------------

# ⭐ Bonus: Type Casting

``` python
a = "10"
b = int(a)
```

------------------------------------------------------------------------

# 🏁 Final Tip

> 💡 रोज practice karo --- coding likhne se hi aati hai!

------------------------------------------------------------------------

# 🔥 Made by Jai Kishan 😎
# 🐍 Python 100 Days of Code
## 📘 README Notes (Lecture 30–60)

## Topics Covered
- Virtual Environment
- Object-Oriented Programming (OOP)
- Classes and Objects
- Constructors (__init__)
- Instance & Class Variables
- Methods
- Inheritance
- Encapsulation
- Polymorphism
- Operator Overloading
- Static Methods
- Class Methods
- Magic (Dunder) Methods
- Exception Handling
- File Handling (Revision)
- Modules & Packages
- And related practice programs

---

## Classes and Objects

### What is a Class?
A class is a blueprint for creating objects.

### Example

```python# 🐍 Python Master Notes

# 📂 File Handling in Python

> "File Handling is used to create, read, write, append and manage files permanently."

---

# 📖 What is File Handling?

File Handling allows us to work with files stored on our computer.

Using File Handling, we can:

- 📄 Read data from a file
- ✍ Write data into a file
- ➕ Append new data
- 🆕 Create new files
- ❌ Delete files (using `os` module)

---

# 🚀 Why File Handling?

- Save user data permanently
- Store reports
- Create log files
- Save project data
- Read configuration files

---

# 📌 open() Function

The `open()` function is used to open a file.

## Syntax

```python
file = open("filename.txt", "mode")
```

Example

```python
file = open("student.txt", "r")
print(file.read())
file.close()
```

---

# 📂 File Modes

| Mode | Description |
|------|-------------|
| `r` | Read file |
| `w` | Write (Overwrite existing file) |
| `a` | Append data |
| `x` | Create new file |
| `t` | Text mode (Default) |
| `b` | Binary mode |

Example

```python
open("data.txt", "r")
open("data.txt", "w")
open("data.txt", "a")
open("image.png", "rb")
```

---

# 📖 Reading Files

## 1. read()

Reads the complete file.

```python
file = open("data.txt", "r")
print(file.read())
file.close()
```

---

## 2. readline()

Reads only one line.

```python
file = open("data.txt", "r")

print(file.readline())
print(file.readline())

file.close()
```

---

## 3. readlines()

Returns all lines as a list.

```python
file = open("data.txt", "r")

print(file.readlines())

file.close()
```

Output

```python
['Hello\n', 'Python\n']
```

---

# ✍ Writing Files

```python
file = open("data.txt", "w")

file.write("Hello Python")

file.close()
```

⚠️ **Warning**

`w` mode removes all previous data before writing.

---

# ➕

## Append Mode

```python
file = open("data.txt", "a")

file.write("\nWelcome")

file.close()
```

Output

```
Hello Python
Welcome
```

---

# 🆕

## Create New File

```python
file = open("new.txt", "x")

file.close()
```

If the file already exists, Python raises an error.

---

# ✅ Best Practice

Use the `with` statement.

```python
with open("data.txt", "r") as file:
    print(file.read())
```

Advantages

- No need to call `close()`
- Automatically closes the file
- Cleaner code

---

# 📌 Important Methods

## close()

```python
file.close()
```

Closes the file.

---

## seek()

Moves the cursor to a specific position.

```python
file = open("data.txt", "r")

file.seek(5)

print(file.read())
```

---

## tell()

Returns the current cursor position.

```python
file = open("data.txt", "r")

print(file.tell())
```

---

## truncate()

Reduces the size of the file.

```python
with open("sample.txt","w") as file:
    file.write("Hello Python")
    file.truncate(5)
```

Output

```
Hello
```

---

# ❌ Common Mistakes

- Forgetting to close files
- Using `w` mode accidentally
- Wrong file path
- Writing in read mode
- Reading from a closed file

---

# 💡 Interview Questions

## Q1. Difference between `w` and `a`?

| `w` | `a` |
|------|------|
| Overwrites file | Adds data at the end |
| Deletes previous content | Keeps previous content |

---

## Q2. Why use `with open()`?

Because it automatically closes the file and prevents resource leaks.

---

## Q3. Difference between `read()`, `readline()` and `readlines()`?

| Method | Returns |
|---------|----------|
| `read()` | Entire file |
| `readline()` | One line |
| `readlines()` | List of all lines |

---

# 🏋 Practice Programs

### Beginner

- Save student name
- Read file
- Append new data

### Intermediate

- Notes App
- Contact Book
- Student Record System

### Advanced

- Employee Management System
- Library Management System
- Banking Record System

---

# 📝 Quick Revision

- `open()` → Opens a file
- `r` → Read
- `w` → Write (Overwrite)
- `a` → Append
- `x` → Create
- `read()` → Read complete file
- `readline()` → Read one line
- `readlines()` → Read all lines
- `seek()` → Move cursor
- `tell()` → Current cursor position
- `truncate()` → Reduce file size
- `with open()` → Best practice
# 🐍 Python Master Notes

# 📦 Topic 2 : Object-Oriented Programming (OOP)

> **Object-Oriented Programming (OOP)** is a programming paradigm that organizes code using **classes** and **objects**. It makes programs more reusable, modular, and easier to maintain.

---

# 📖 What is OOP?

OOP is a way of writing programs by representing real-world objects.

Instead of writing everything in functions, we create **classes** and then create **objects** from those classes.

### Real-Life Examples

| Real World | Python |
|------------|--------|
| Car | Object |
| Student | Object |
| Mobile | Object |
| Bank Account | Object |

---

# 🤔 Why OOP?

Without OOP:
- Code becomes repetitive.
- Large projects become difficult to manage.
- Reusability is low.

With OOP:
- ✅ Code Reusability
- ✅ Better Organization
- ✅ Easy Maintenance
- ✅ Security
- ✅ Easy to Understand

---

# 📚 Important Terms

| Term | Meaning |
|------|----------|
| Class | Blueprint |
| Object | Instance of a class |
| Attribute | Variable inside a class |
| Method | Function inside a class |

---

# 🏗 What is a Class?

A **class** is a blueprint used to create objects.

### Syntax

```python
class Student:
    pass
```

Example

```python
class Student:
    pass
```

---

# 👤 What is an Object?

An object is an instance of a class.

```python
class Student:
    pass

s1 = Student()
s2 = Student()
```

Here,

- `Student` → Class
- `s1` → Object
- `s2` → Object

---

# 🎯 Real Example

```python
class Student:
    name = "Jai"
    marks = 95

s1 = Student()

print(s1.name)
print(s1.marks)
```

Output

```
Jai
95
```

---

# 📌 Attributes

Attributes are variables that belong to a class or object.

Example

```python
class Mobile:

    brand = "Samsung"

m1 = Mobile()

print(m1.brand)
```

---

# 📌 Methods

Methods are functions inside a class.

Example

```python
class Student:

    def show(self):
        print("Welcome")

s1 = Student()

s1.show()
```

Output

```
Welcome
```

---

# 🌍 Real-Life Example

```python
class Car:

    brand = "BMW"

    def start(self):
        print("Car Started")

car1 = Car()

print(car1.brand)

car1.start()
```

Output

```
BMW
Car Started
```

---

# 📌 Advantages of OOP

- Code Reusability
- Better Security
- Easy Debugging
- Easy Maintenance
- Better Structure
- Real-World Modeling
- Modular Programming

---

# 📂 OOP Pillars

Python OOP has four major pillars:

1. Encapsulation
2. Inheritance
3. Polymorphism
4. Abstraction

These topics are covered separately in later notes.

---

# ❌ Common Mistakes

### Mistake 1

```python
class Student

    pass
```

Missing `:` after class name.

---

### Mistake 2

```python
class Student:
    pass

print(name)
```

Wrong.

Correct

```python
s = Student()
```

---

### Mistake 3

Trying to call a method without an object.

Wrong

```python
show()
```

Correct

```python
s.show()
```

---

# 💡 Interview Questions

### Q1. What is OOP?

Object-Oriented Programming is a programming paradigm that uses classes and objects to organize code.

---

### Q2. What is a Class?

A class is a blueprint used to create objects.

---

### Q3. What is an Object?

An object is an instance of a class.

---

### Q4. Difference between Class and Object?

| Class | Object |
|--------|---------|
| Blueprint | Real Instance |
| Template | Actual Entity |
| No Memory Until Object Exists | Uses Memory |

---

# 🏋 Practice Programs

### Easy

- Student Class
- Mobile Class
- Car Class

### Medium

- Employee Class
- Bank Account Class
- Laptop Class

### Advanced

- Library Management System
- School Management System
- Hospital Management System

---

# 📝 Quick Revision

- OOP = Object-Oriented Programming
- Class = Blueprint
- Object = Instance of a Class
- Attribute = Variable
- Method = Function inside a class
- OOP makes code reusable and organized.
- Objects are created using classes.

---

# 🚀 What's Next?

📌 **Topic 3 : Constructor (`__init__`)**

In the next notes, you'll learn:
- What is a constructor?
- Why `__init__()` is used
- What is `self`?
- How objects are initialized
- Constructor examples and interview questions
---

# 🎯 Summary

File Handling is one of the most important Python topics. It is used in almost every real-world project because it allows programs to store and retrieve data permanently.
class Student:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks# 🐍 Python Master Notes

# 🏗️ Topic 3 : Constructor (`__init__()`)

> **A constructor is a special method that is automatically called whenever an object of a class is created.**

---

# 📖 What is a Constructor?

A **constructor** is a special method in Python that initializes an object.

In Python, the constructor is written as:

```python
__init__()
```

It is automatically executed when an object is created.

---

# 🤔 Why Do We Use Constructors?

Without a constructor, we have to assign values manually.

Example (Without Constructor)

```python
class Student:
    pass

s1 = Student()

s1.name = "Jai"
s1.age = 16

print(s1.name)
print(s1.age)
```

This works, but it becomes difficult when there are many objects.

Using a constructor makes the code cleaner and more efficient.

---

# 📌 Syntax

```python
class ClassName:

    def __init__(self):
        # Initialization Code
```

---

# ✅ Simple Constructor

```python
class Student:

    def __init__(self):
        print("Object Created")

s1 = Student()
```

### Output

```
Object Created
```

The `__init__()` method is called automatically when `Student()` is executed.

---

# 📌 Constructor with Parameters

```python
class Student:

    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

s1 = Student("Jai", 95)

print(s1.name)
print(s1.marks)
```

### Output

```
Jai
95
```

---

# 📌 What is `self`?

`self` refers to the **current object**.

It allows us to access the attributes and methods of the object.

Example

```python
class Student:

    def __init__(self, name):
        self.name = name

s1 = Student("Jai")

print(s1.name)
```

Here,

- `self.name` → Attribute of the current object
- `"Jai"` → Value passed while creating the object

---

# 📌 Multiple Objects

```python
class Student:

    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

s1 = Student("Jai", 90)
s2 = Student("Rahul", 85)

print(s1.name, s1.marks)
print(s2.name, s2.marks)
```

### Output

```
Jai 90
Rahul 85
```

Each object stores its own data independently.

---

# 📌 Adding Methods

```python
class Student:

    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def show(self):
        print(self.name, self.marks)

s1 = Student("Jai", 95)

s1.show()
```

### Output

```
Jai 95
```

---

# 🌍 Real-Life Example

```python
class Mobile:

    def __init__(self, brand, price):
        self.brand = brand
        self.price = price

    def details(self):
        print("Brand :", self.brand)
        print("Price :", self.price)

m1 = Mobile("Samsung", 25000)

m1.details()
```

### Output

```
Brand : Samsung
Price : 25000
```

---

# 📌 Types of Constructors

## 1. Default Constructor

```python
class Demo:

    def __init__(self):
        print("Hello")
```

No extra arguments are passed.

---

## 2. Parameterized Constructor

```python
class Demo:

    def __init__(self, name):
        self.name = name
```

Values are passed while creating the object.

---

# ❌ Common Mistakes

### Missing `self`

❌ Wrong

```python
class Student:

    def __init__(name):
        pass
```

✅ Correct

```python
class Student:

    def __init__(self, name):
        self.name = name
```

---

### Forgetting `self`

❌ Wrong

```python
name = name
```

✅ Correct

```python
self.name = name
```

---

### Wrong Number of Arguments

```python
Student()
```

If the constructor expects parameters, Python raises a `TypeError`.

---

# 💡 Interview Questions

### Q1. What is a constructor?

A constructor is a special method that automatically runs when an object is created.

---

### Q2. What is the name of the constructor in Python?

```python
__init__()
```

---

### Q3. Is calling `__init__()` manually necessary?

No. Python calls it automatically when an object is created.

---

### Q4. What is `self`?

`self` is a reference to the current object of the class.

---

### Q5. Can a class exist without a constructor?

Yes. Python provides a default constructor if you don't define one.

---

# 🏋 Practice Programs

### Beginner

- Student Class
- Mobile Class
- Car Class

### Intermediate

- Employee Details
- Bank Account
- Laptop Information

### Advanced

- Library Management System
- School Management System
- ATM Simulation

---

# 📝 Quick Revision

- `__init__()` is a constructor.
- It runs automatically when an object is created.
- `self` refers to the current object.
- Constructors initialize object data.
- Constructors can be default or parameterized.
- Use `self.variable = value` to create object attributes.

---

# 🚀 What's Next?

📌 **Topic 4 : `self` Keyword**

In the next topic, we'll understand:
- Why `self` is required
- How Python passes `self` automatically
- `self` vs normal variables
- Common mistakes with `self`
- Interview questions and examples

    def show(self):
        print(self.name, self.marks)# 🐍 Python Master Notes

# 👤 Topic 4 : `self` Keyword

> **`self` is a reference to the current object of a class. It allows an object to access its own variables and methods.**

---

# 📖 What is `self`?

`self` is the first parameter of every **instance method** in a class.

It represents **the current object** that is calling the method.

When an object calls a method, Python automatically passes that object as the first argument.

---

# 🤔 Why Do We Use `self`?

Without `self`, Python cannot identify which object's data should be used.

Example:

```python
class Student:

    def __init__(self, name):
        self.name = name
```

Here,

- `self.name` → Variable inside the object
- `name` → Value received from the user

---

# 📌 Syntax

```python
class ClassName:

    def method(self):
        pass
```

---

# ✅ Example 1

```python
class Student:

    def __init__(self, name):
        self.name = name

    def show(self):
        print(self.name)

s1 = Student("Jai")

s1.show()
```

### Output

```
Jai
```

---

# ✅ Example 2

```python
class Car:

    def __init__(self, brand):
        self.brand = brand

    def start(self):
        print(self.brand, "Started")

c1 = Car("BMW")

c1.start()
```

### Output

```
BMW Started
```

---

# 🔍 How Python Works Internally

When you write:

```python
s1.show()
```

Python internally does this:

```python
Student.show(s1)
```

So, `self` automatically becomes `s1`.

---

# 📌 Multiple Objects Example

```python
class Student:

    def __init__(self, name):
        self.name = name

    def show(self):
        print(self.name)

s1 = Student("Jai")
s2 = Student("Rahul")

s1.show()
s2.show()
```

### Output

```
Jai
Rahul
```

Each object has its own data.

---

# 📌 Accessing Variables Using `self`

```python
class Employee:

    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

    def details(self):
        print(self.name)
        print(self.salary)

e1 = Employee("Amit", 50000)

e1.details()
```

---

# ❌ Without `self`

```python
class Student:

    def __init__(self, name):
        name = name
```

This does **not** create an object attribute.

Correct:

```python
self.name = name
```

---

# 📌 Accessing Methods Using `self`

A method can call another method using `self`.

```python
class Demo:

    def hello(self):
        print("Hello")

    def welcome(self):
        self.hello()
        print("Welcome")

d = Demo()

d.welcome()
```

### Output

```
Hello
Welcome
```

---

# 📌 Can We Use Another Name Instead of `self`?

Yes.

```python
class Demo:

    def __init__(myobject):
        print("Hello")
```

This code works.

But according to Python conventions (**PEP 8**), always use **`self`**.

---

# ❌ Common Mistakes

### Mistake 1

```python
class Student:

    def show():
        print("Hello")
```

Correct

```python
class Student:

    def show(self):
        print("Hello")
```

---

### Mistake 2

```python
name = name
```

Correct

```python
self.name = name
```

---

### Mistake 3

Trying to access object variables without `self`.

Wrong

```python
print(name)
```

Correct

```python
print(self.name)
```

---

# 💡 Interview Questions

### Q1. What is `self`?

`self` is a reference to the current object of a class.

---

### Q2. Is `self` a keyword?

❌ No.

It is **not** a Python keyword.

It is only a naming convention.

---

### Q3. Who passes `self`?

Python automatically passes the current object when a method is called.

---

### Q4. Can we change the name of `self`?

Yes, but it is not recommended.

Always use `self` for readability.

---

# 🏋 Practice Programs

### Beginner

- Student Class
- Car Class
- Mobile Class

### Intermediate

- Employee Details
- Bank Account
- Library Book Class

### Advanced

- School Management System
- Hospital Management System
- ATM Simulation

---

# 📝 Quick Revision

- `self` refers to the current object.
- It is the first parameter of instance methods.
- Python passes `self` automatically.
- Use `self.variable` to create object attributes.
- Use `self.method()` to call another method in the same class.
- `self` is **not** a keyword; it is a convention.

---

# 🧠 Key Takeaway

Whenever you see:

```python
self.name = name
```

Remember:

- Left side (`self.name`) → Object attribute
- Right side (`name`) → Value passed by the user

---

# 🚀 What's Next?

📌 **Topic 5 : Instance Variables & Class Variables**

In the next topic, you'll learn:
- Instance Variables
- Class Variables
- Difference between them
- Real-world examples
- Common mistakes
- Interview questions

- # 🐍 Python Master Notes

# 👤 Topic 4 : `self` Keyword

> **`self` is a reference to the current object of a class. It allows an object to access its own variables and methods.**

---

# 📖 What is `self`?

`self` is the first parameter of every **instance method** in a class.

It represents **the current object** that is calling the method.

When an object calls a method, Python automatically passes that object as the first argument.

---

# 🤔 Why Do We Use `self`?

Without `self`, Python cannot identify which object's data should be used.

Example:

```python
class Student:

    def __init__(self, name):
        self.name = name
```

Here,

- `self.name` → Variable inside the object
- `name` → Value received from the user

---

# 📌 Syntax

```python
class ClassName:

    def method(self):
        pass
```

---

# ✅ Example 1

```python
class Student:

    def __init__(self, name):
        self.name = name

    def show(self):
        print(self.name)

s1 = Student("Jai")

s1.show()
```

### Output

```
Jai
```

---

# ✅ Example 2

```python
class Car:

    def __init__(self, brand):
        self.brand = brand

    def start(self):
        print(self.brand, "Started")

c1 = Car("BMW")

c1.start()
```

### Output

```
BMW Started
```

---

# 🔍 How Python Works Internally

When you write:

```python
s1.show()
```

Python internally does this:

```python
Student.show(s1)
```

So, `self` automatically becomes `s1`.

---

# 📌 Multiple Objects Example

```python
class Student:

    def __init__(self, name):
        self.name = name

    def show(self):
        print(self.name)

s1 = Student("Jai")
s2 = Student("Rahul")

s1.show()
s2.show()
```

### Output

```
Jai
Rahul
```

Each object has its own data.

---

# 📌 Accessing Variables Using `self`

```python
class Employee:

    def __init__(self, name, salary):
        self.name = name
        self.salary = salary

    def details(self):
        print(self.name)
        print(self.salary)

e1 = Employee("Amit", 50000)

e1.details()
```

---

# ❌ Without `self`

```python
class Student:

    def __init__(self, name):
        name = name
```

This does **not** create an object attribute.

Correct:

```python
self.name = name
```

---

# 📌 Accessing Methods Using `self`

A method can call another method using `self`.

```python
class Demo:

    def hello(self):
        print("Hello")

    def welcome(self):
        self.hello()
        print("Welcome")

d = Demo()

d.welcome()
```

### Output

```
Hello
Welcome
```

---

# 📌 Can We Use Another Name Instead of `self`?

Yes.

```python
class Demo:

    def __init__(myobject):
        print("Hello")
```

This code works.

But according to Python conventions (**PEP 8**), always use **`self`**.

---

# ❌ Common Mistakes

### Mistake 1

```python
class Student:

    def show():
        print("Hello")
```

Correct

```python
class Student:

    def show(self):
        print("Hello")
```

---

### Mistake 2

```python
name = name
```

Correct

```python
self.name = name
```

---

### Mistake 3

Trying to access object variables without `self`.

Wrong

```python
print(name)
```

Correct

```python
print(self.name)
```

---

# 💡 Interview Questions

### Q1. What is `self`?

`self` is a reference to the current object of a class.

---

### Q2. Is `self` a keyword?

❌ No.

It is **not** a Python keyword.

It is only a naming convention.

---

### Q3. Who passes `self`?

Python automatically passes the current object when a method is called.

---

### Q4. Can we change the name of `self`?

Yes, but it is not recommended.

Always use `self` for readability.

---

# 🏋 Practice Programs

### Beginner

- Student Class
- Car Class
- Mobile Class

### Intermediate

- Employee Details
- Bank Account
- Library Book Class

### Advanced

- School Management System
- Hospital Management System
- ATM Simulation

---

# 📝 Quick Revision

- `self` refers to the current object.
- It is the first parameter of instance methods.
- Python passes `self` automatically.
- Use `self.variable` to create object attributes.
- Use `self.method()` to call another method in the same class.
- `self` is **not** a keyword; it is a convention.

---

# 🧠 Key Takeaway

Whenever you see:

```python
self.name = name
```

Remember:

- Left side (`self.name`) → Object attribute
- Right side (`name`) → Value passed by the user

---

# 🚀 What's Next?

📌 **Topic 5 : Instance Variables & Class Variables**

In the next topic, you'll learn:
- Instance Variables
- Class Variables
- Difference between them
- Real-world examples
- Common mistakes
- Interview questions
