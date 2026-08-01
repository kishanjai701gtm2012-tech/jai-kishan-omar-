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

```python
class Student:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def show(self):
        print(self.name, self.marks)
