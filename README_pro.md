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

---

# 🎯 Summary

File Handling is one of the most important Python topics. It is used in almost every real-world project because it allows programs to store and retrieve data permanently.
class Student:
    def __init__(self, name, marks):
        self.name = name
        self.marks = marks

    def show(self):
        print(self.name, self.marks)
