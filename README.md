# 📘 Python Notes (Beginner to Intermediate)

## 1️⃣ Variables

Variable ek container hota hai jo data store karta hai.

``` python
name = "Jai"
age = 16
```

------------------------------------------------------------------------

## 2️⃣ Data Types

-   **int** → Integer
-   **float** → Decimal
-   **str** → String
-   **bool** → True/False

``` python
a = 10
b = 3.14
c = "Hello"
d = True
```

------------------------------------------------------------------------

## 3️⃣ List

-   Ordered & Mutable collection

``` python
fruits = ["apple", "banana", "mango"]
```

### Methods:

-   append()
-   remove()
-   pop()

------------------------------------------------------------------------

## 4️⃣ Tuple

-   Immutable collection

``` python
numbers = (1, 2, 3)
```

------------------------------------------------------------------------

## 5️⃣ f-String

``` python
name = "Jai"
print(f"My name is {name}")
```

------------------------------------------------------------------------

## 6️⃣ Conditionals

``` python
age = 18

if age >= 18:
    print("You can vote")
else:
    print("You cannot vote")
```

------------------------------------------------------------------------

## 7️⃣ Loops

### for loop

``` python
for i in range(5):
    print(i)
```

### while loop

``` python
i = 1
while i <= 5:
    print(i)
    i += 1
```

------------------------------------------------------------------------

## 8️⃣ Functions

``` python
def greet(name):
    print("Hello", name)

greet("Jai")
```

------------------------------------------------------------------------

## 9️⃣ Input / Output

``` python
name = input("Enter your name: ")
print(name)
```

------------------------------------------------------------------------

## 🔟 Operators

-   Arithmetic: + - \* /
-   Comparison: == != \> \<

------------------------------------------------------------------------

## ⭐ Bonus: Type Casting

``` python
a = "10"
b = int(a)
```

------------------------------------------------------------------------

## 🚀 Pro Tip

Practice daily. Code likhna zaroori hai.
Ab slicing

example  ke saht 
1. Pehla letter
word[0]
Output:
k

2. Last letter
word[-1]
Output:
n


3. Pehle letter ke baad sab
word[1:]
Output:
ishan


4. Last letter ko chhodkar sab
word[:-1]
Output:
kisha


5. Reverse
word[::-1]
Output:
nahsik
Ab tumhari exercise ka hint

Agar "kishan" ko badalna hai aur pehla letter last me bhejna hai, to:

word[1:] + word[0]

Socho iska ou
