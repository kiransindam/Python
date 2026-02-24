# 🐍 Python Programming Course — Beginner to Advanced

<div align="center">

![Python](https://img.shields.io/badge/Python-3.10%2B-blue?style=for-the-badge&logo=python&logoColor=white)
![Level](https://img.shields.io/badge/Level-Beginner%20to%20Advanced-green?style=for-the-badge)
![License](https://img.shields.io/badge/License-MIT-yellow?style=for-the-badge)
![Status](https://img.shields.io/badge/Status-Active-brightgreen?style=for-the-badge)

**A structured, hands-on Python course from absolute zero to professional-level programming.**

</div>

---

## 📌 Table of Contents

1. [About This Course](#about-this-course)
2. [Who Is This For?](#who-is-this-for)
3. [Course Structure](#course-structure)
4. [Setup & Installation](#setup--installation)
5. [🟢 Module 1 — Beginner](#-module-1--beginner)
6. [🟡 Module 2 — Intermediate](#-module-2--intermediate)
7. [🔴 Module 3 — Advanced](#-module-3--advanced)
8. [🚀 Module 4 — Expert & Real-World Projects](#-module-4--expert--real-world-projects)
9. [Mini Projects by Level](#mini-projects-by-level)
10. [Cheat Sheets](#cheat-sheets)
11. [Learning Resources](#learning-resources)
12. [Contributing](#contributing)
13. [License](#license)

---

## About This Course

This is a **free, open-source Python programming course** designed to take anyone — regardless of background — from writing their very first line of code to building real-world applications. Every section includes clear explanations, practical code examples, and mini projects to reinforce learning.

### 🎯 What You Will Learn
- Python fundamentals: syntax, data types, control flow
- Functions, modules, and error handling
- Object-Oriented Programming (OOP)
- File handling, regular expressions, and databases
- Web scraping, APIs, and automation
- Data structures and algorithms
- Testing, debugging, and clean code practices
- Real-world projects in web, data, and automation

---

## Who Is This For?

| Audience | Description |
|---|---|
| 🧑‍🎓 Absolute Beginners | No prior coding experience needed |
| 💼 Career Switchers | Transitioning from another field into tech |
| 📊 Data Enthusiasts | Looking to use Python for data and analytics |
| 🔧 Developers | Wanting to add Python to their toolkit |
| 🎓 Students | Supplementing university coursework |

---

## Course Structure

```
Python Course
│
├── Module 1 — Beginner         (Weeks 1–3)
│   ├── Python Basics
│   ├── Control Flow
│   ├── Functions
│   └── Data Structures
│
├── Module 2 — Intermediate     (Weeks 4–6)
│   ├── Object-Oriented Programming
│   ├── File & Exception Handling
│   ├── Modules & Packages
│   └── Iterators & Generators
│
├── Module 3 — Advanced         (Weeks 7–9)
│   ├── Decorators & Closures
│   ├── Concurrency & Multithreading
│   ├── Databases (SQL + ORM)
│   └── Testing & Debugging
│
└── Module 4 — Expert           (Weeks 10–12)
    ├── Web Development (Flask)
    ├── Web Scraping & APIs
    ├── Automation
    └── Capstone Projects
```

---

## Setup & Installation

### Step 1: Install Python

Download the latest version from [python.org](https://www.python.org/downloads/)

```bash
# Verify installation
python --version       # Python 3.10+
pip --version          # pip 23+
```

### Step 2: Install a Code Editor

| Editor | Download | Best For |
|---|---|---|
| VS Code | [code.visualstudio.com](https://code.visualstudio.com/) | General purpose |
| PyCharm | [jetbrains.com](https://www.jetbrains.com/pycharm/) | Professional dev |
| Jupyter | `pip install notebook` | Data & learning |
| Thonny | [thonny.org](https://thonny.org/) | Absolute beginners |

### Step 3: Set Up a Virtual Environment

```bash
# Create environment
python -m venv venv

# Activate — Windows
venv\Scripts\activate

# Activate — macOS/Linux
source venv/bin/activate

# Install dependencies
pip install -r requirements.txt
```

### Step 4: Clone This Repository

```bash
git clone https://github.com/yourusername/python-course.git
cd python-course
```

---

## 🟢 Module 1 — Beginner

> **Goal:** Understand Python syntax, work with data types, and write basic programs.
> **Duration:** Weeks 1–3 | **Prerequisites:** None

---

### 1.1 Hello, Python!

```python
# Your very first Python program
print("Hello, World!")
print("Welcome to Python Programming!")

# Python is readable — it looks like plain English
name = "Alice"
age = 25
print(f"My name is {name} and I am {age} years old.")
```

---

### 1.2 Variables & Data Types

```python
# ── Strings ──────────────────────────────────────────
name      = "Python"         # str
greeting  = 'Hello!'         # str (single or double quotes)
multi     = """This is a
multi-line string."""

# String methods
print(name.upper())          # PYTHON
print(name.lower())          # python
print(name.replace("P", "J"))# Jython
print(len(name))             # 6
print(name[0])               # P (indexing)
print(name[1:4])             # yth (slicing)
print(f"I love {name}!")     # f-string formatting

# ── Numbers ──────────────────────────────────────────
integer_num = 42             # int
float_num   = 3.14           # float
complex_num = 2 + 3j         # complex

# Arithmetic operators
print(10 + 3)                # 13  addition
print(10 - 3)                # 7   subtraction
print(10 * 3)                # 30  multiplication
print(10 / 3)                # 3.33 division
print(10 // 3)               # 3   floor division
print(10 % 3)                # 1   modulo
print(10 ** 3)               # 1000 exponent

# ── Boolean ──────────────────────────────────────────
is_active = True
is_done   = False

print(True and False)        # False
print(True or False)         # True
print(not True)              # False

# ── Type Conversion ──────────────────────────────────
print(int("42"))             # 42
print(float("3.14"))         # 3.14
print(str(100))              # "100"
print(bool(0))               # False
print(bool(1))               # True
print(type(42))              # <class 'int'>
```

---

### 1.3 User Input

```python
# Getting input from the user
name = input("Enter your name: ")
age  = int(input("Enter your age: "))   # Convert to int
print(f"Hello {name}! You are {age} years old.")

# Simple calculator
num1 = float(input("Enter first number: "))
num2 = float(input("Enter second number: "))
print(f"Sum     : {num1 + num2}")
print(f"Product : {num1 * num2}")
```

---

### 1.4 Control Flow

```python
# ── If / Elif / Else ─────────────────────────────────
score = 85

if score >= 90:
    grade = "A"
elif score >= 80:
    grade = "B"
elif score >= 70:
    grade = "C"
elif score >= 60:
    grade = "D"
else:
    grade = "F"

print(f"Your grade is: {grade}")   # B

# Ternary (one-line if)
status = "Pass" if score >= 50 else "Fail"

# ── Comparison & Logical Operators ───────────────────
x = 10
print(x > 5 and x < 20)    # True
print(x == 10 or x == 20)  # True
print(x not in [1, 2, 3])  # True
```

---

### 1.5 Loops

```python
# ── For Loop ─────────────────────────────────────────
for i in range(5):
    print(i)                 # 0 1 2 3 4

for i in range(1, 11, 2):
    print(i)                 # 1 3 5 7 9

# Looping over a string
for char in "Python":
    print(char)

# ── While Loop ───────────────────────────────────────
count = 0
while count < 5:
    print(f"Count: {count}")
    count += 1

# ── Loop Control ─────────────────────────────────────
for num in range(10):
    if num == 3:
        continue             # Skip 3
    if num == 7:
        break                # Stop at 7
    print(num)

# ── List Comprehension ───────────────────────────────
squares   = [x**2 for x in range(10)]
evens     = [x for x in range(20) if x % 2 == 0]
uppercase = [w.upper() for w in ["hello", "world"]]
```

---

### 1.6 Data Structures

```python
# ── Lists (ordered, mutable) ─────────────────────────
fruits = ["apple", "banana", "cherry"]
fruits.append("date")         # Add at end
fruits.insert(1, "avocado")   # Insert at index
fruits.remove("banana")       # Remove by value
popped = fruits.pop()         # Remove & return last
fruits.sort()                 # Sort in place
fruits.reverse()              # Reverse in place
print(len(fruits))            # Length
print("apple" in fruits)      # Membership check

# Nested list
matrix = [[1, 2, 3], [4, 5, 6], [7, 8, 9]]
print(matrix[1][2])           # 6

# ── Tuples (ordered, immutable) ──────────────────────
coordinates = (28.61, 77.20)
x, y = coordinates            # Unpacking
print(x, y)

# ── Sets (unordered, unique) ─────────────────────────
unique = {1, 2, 3, 3, 4}     # {1, 2, 3, 4} — duplicates removed
unique.add(5)
unique.discard(2)
set_a = {1, 2, 3}
set_b = {2, 3, 4}
print(set_a & set_b)          # Intersection: {2, 3}
print(set_a | set_b)          # Union: {1, 2, 3, 4}
print(set_a - set_b)          # Difference: {1}

# ── Dictionaries (key-value pairs) ───────────────────
student = {
    "name"   : "Alice",
    "age"    : 25,
    "grades" : [90, 85, 88]
}

print(student["name"])          # Alice
print(student.get("gpa", 0.0)) # 0.0 (default if missing)
student["city"] = "Delhi"       # Add key
del student["age"]              # Delete key
print(student.keys())
print(student.values())
print(student.items())          # Key-value pairs

# Dictionary comprehension
squares = {x: x**2 for x in range(6)}  # {0:0, 1:1, 2:4 ...}
```

---

### 1.7 Functions

```python
# ── Basic Function ───────────────────────────────────
def greet(name):
    """Prints a greeting message."""
    print(f"Hello, {name}!")

greet("Alice")

# ── Parameters & Return ──────────────────────────────
def add(a, b):
    return a + b

result = add(3, 5)    # 8

# ── Default Arguments ────────────────────────────────
def power(base, exp=2):
    return base ** exp

print(power(3))       # 9
print(power(3, 3))    # 27

# ── *args and **kwargs ───────────────────────────────
def total(*args):
    return sum(args)

print(total(1, 2, 3, 4))  # 10

def show_info(**kwargs):
    for key, value in kwargs.items():
        print(f"{key}: {value}")

show_info(name="Alice", age=25, city="Delhi")

# ── Lambda Functions ─────────────────────────────────
square   = lambda x: x ** 2
multiply = lambda x, y: x * y

nums = [5, 2, 8, 1, 9]
nums.sort(key=lambda x: -x)    # Sort descending

# ── Scope ────────────────────────────────────────────
global_var = "I am global"

def show_scope():
    local_var = "I am local"
    print(global_var)
    print(local_var)

show_scope()
```

---

## 🟡 Module 2 — Intermediate

> **Goal:** Write reusable, structured, and robust Python code.
> **Duration:** Weeks 4–6 | **Prerequisites:** Module 1

---

### 2.1 Object-Oriented Programming (OOP)

```python
# ── Classes & Objects ────────────────────────────────
class Person:
    species = "Homo Sapiens"       # Class attribute

    def __init__(self, name, age):
        self.name = name           # Instance attribute
        self.age  = age

    def introduce(self):
        return f"Hi, I'm {self.name} and I'm {self.age} years old."

    def __str__(self):             # String representation
        return f"Person({self.name}, {self.age})"

    def __repr__(self):            # Developer representation
        return f"Person(name='{self.name}', age={self.age})"


p1 = Person("Alice", 25)
print(p1.introduce())
print(p1)

# ── Inheritance ──────────────────────────────────────
class Employee(Person):
    def __init__(self, name, age, emp_id, department):
        super().__init__(name, age)
        self.emp_id     = emp_id
        self.department = department

    def introduce(self):           # Method overriding
        base = super().introduce()
        return f"{base} I work in {self.department}."

    @property
    def profile(self):             # Property decorator
        return f"{self.name} [{self.emp_id}]"


emp = Employee("Bob", 30, "E101", "Engineering")
print(emp.introduce())
print(emp.profile)

# ── Encapsulation ────────────────────────────────────
class BankAccount:
    def __init__(self, owner, balance=0):
        self.owner    = owner
        self.__balance = balance    # Private attribute

    def deposit(self, amount):
        if amount > 0:
            self.__balance += amount

    def withdraw(self, amount):
        if 0 < amount <= self.__balance:
            self.__balance -= amount
        else:
            print("Insufficient funds!")

    def get_balance(self):
        return self.__balance


account = BankAccount("Alice", 1000)
account.deposit(500)
account.withdraw(200)
print(account.get_balance())       # 1300

# ── Polymorphism ─────────────────────────────────────
class Shape:
    def area(self):
        raise NotImplementedError

class Circle(Shape):
    def __init__(self, radius):
        self.radius = radius
    def area(self):
        return 3.14159 * self.radius ** 2

class Rectangle(Shape):
    def __init__(self, width, height):
        self.width  = width
        self.height = height
    def area(self):
        return self.width * self.height

shapes = [Circle(5), Rectangle(4, 6)]
for shape in shapes:
    print(f"{shape.__class__.__name__}: Area = {shape.area():.2f}")
```

---

### 2.2 Exception Handling

```python
# ── Try / Except / Else / Finally ────────────────────
def divide(a, b):
    try:
        result = a / b
    except ZeroDivisionError:
        print("Error: Cannot divide by zero!")
        return None
    except TypeError as e:
        print(f"Type error: {e}")
        return None
    else:
        print("Division successful!")
        return result
    finally:
        print("Execution complete.")   # Always runs


print(divide(10, 2))
print(divide(10, 0))

# ── Custom Exceptions ────────────────────────────────
class InsufficientFundsError(Exception):
    def __init__(self, amount, balance):
        self.amount  = amount
        self.balance = balance
        super().__init__(
            f"Cannot withdraw ₹{amount}. Balance: ₹{balance}"
        )


def withdraw(balance, amount):
    if amount > balance:
        raise InsufficientFundsError(amount, balance)
    return balance - amount


try:
    new_balance = withdraw(500, 1000)
except InsufficientFundsError as e:
    print(e)
```

---

### 2.3 File Handling

```python
import os
import json
import csv

# ── Text Files ───────────────────────────────────────
# Write
with open("notes.txt", "w") as f:
    f.write("Line 1: Python is great!\n")
    f.write("Line 2: Keep learning!\n")

# Read all
with open("notes.txt", "r") as f:
    content = f.read()

# Read line by line
with open("notes.txt", "r") as f:
    for line in f:
        print(line.strip())

# Append
with open("notes.txt", "a") as f:
    f.write("Line 3: Practice daily!\n")

# ── JSON Files ───────────────────────────────────────
data = {"name": "Alice", "age": 25, "skills": ["Python", "SQL"]}

with open("data.json", "w") as f:
    json.dump(data, f, indent=4)

with open("data.json", "r") as f:
    loaded = json.load(f)
    print(loaded["name"])

# ── CSV Files ────────────────────────────────────────
rows = [["Name", "Age", "City"],
        ["Alice", 25, "Delhi"],
        ["Bob",   30, "Mumbai"]]

with open("people.csv", "w", newline="") as f:
    writer = csv.writer(f)
    writer.writerows(rows)

with open("people.csv", "r") as f:
    reader = csv.DictReader(f)
    for row in reader:
        print(row)

# ── os Module ────────────────────────────────────────
print(os.getcwd())             # Current directory
os.makedirs("output", exist_ok=True)
print(os.listdir("."))
os.rename("notes.txt", "my_notes.txt")
```

---

### 2.4 Modules & Packages

```python
# ── Built-in Modules ─────────────────────────────────
import math
import random
import datetime
import os
import sys

print(math.sqrt(144))          # 12.0
print(math.pi)                 # 3.14159...
print(math.factorial(5))       # 120

print(random.randint(1, 100))  # Random int
print(random.choice(["a","b","c"]))
random.shuffle([1, 2, 3, 4])

now = datetime.datetime.now()
print(now.strftime("%Y-%m-%d %H:%M:%S"))

# ── Creating Your Own Module ─────────────────────────
# File: calculator.py
def add(a, b): return a + b
def sub(a, b): return a - b
def mul(a, b): return a * b
def div(a, b): return a / b if b != 0 else None

# Usage in another file:
# import calculator
# print(calculator.add(5, 3))

# ── Itertools & Functools ────────────────────────────
from itertools import product, permutations, combinations
from functools import reduce, partial

print(list(permutations([1, 2, 3], 2)))
print(list(combinations([1, 2, 3, 4], 2)))

total = reduce(lambda x, y: x + y, [1, 2, 3, 4, 5])
print(total)                   # 15

double = partial(mul, 2)       # Partially applied function
print(double(5))               # 10
```

---

### 2.5 Iterators & Generators

```python
# ── Iterators ────────────────────────────────────────
class CountUp:
    def __init__(self, start, end):
        self.current = start
        self.end     = end

    def __iter__(self):
        return self

    def __next__(self):
        if self.current > self.end:
            raise StopIteration
        val = self.current
        self.current += 1
        return val


for num in CountUp(1, 5):
    print(num)

# ── Generators ───────────────────────────────────────
def fibonacci(n):
    a, b = 0, 1
    for _ in range(n):
        yield a
        a, b = b, a + b


for num in fibonacci(10):
    print(num, end=" ")

# Generator expression (memory-efficient)
squares_gen = (x**2 for x in range(1000000))
print(next(squares_gen))       # 0
print(next(squares_gen))       # 1
```

---

## 🔴 Module 3 — Advanced

> **Goal:** Master Python internals, write performant and professional code.
> **Duration:** Weeks 7–9 | **Prerequisites:** Module 2

---

### 3.1 Decorators & Closures

```python
import time
import functools

# ── Closures ─────────────────────────────────────────
def make_multiplier(factor):
    def multiply(n):
        return n * factor          # Closes over `factor`
    return multiply

triple = make_multiplier(3)
print(triple(5))                   # 15

# ── Decorators ───────────────────────────────────────
def timer(func):
    """Decorator to measure execution time."""
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        start  = time.perf_counter()
        result = func(*args, **kwargs)
        end    = time.perf_counter()
        print(f"{func.__name__} took {end - start:.4f}s")
        return result
    return wrapper


def logger(func):
    """Decorator to log function calls."""
    @functools.wraps(func)
    def wrapper(*args, **kwargs):
        print(f"Calling {func.__name__} with {args}, {kwargs}")
        result = func(*args, **kwargs)
        print(f"{func.__name__} returned {result}")
        return result
    return wrapper


@timer
@logger
def slow_function(n):
    time.sleep(0.1)
    return n ** 2


slow_function(5)

# ── Parameterized Decorators ─────────────────────────
def repeat(times):
    def decorator(func):
        @functools.wraps(func)
        def wrapper(*args, **kwargs):
            for _ in range(times):
                result = func(*args, **kwargs)
            return result
        return wrapper
    return decorator


@repeat(3)
def say_hello():
    print("Hello!")

say_hello()    # Prints Hello! three times
```

---

### 3.2 Concurrency & Multithreading

```python
import threading
import multiprocessing
import asyncio
import concurrent.futures

# ── Threading (I/O-bound tasks) ──────────────────────
def download_file(url, thread_id):
    print(f"Thread {thread_id}: Downloading {url}...")
    time.sleep(2)              # Simulating download
    print(f"Thread {thread_id}: Done!")

threads = []
for i in range(5):
    t = threading.Thread(target=download_file, args=(f"url_{i}", i))
    threads.append(t)
    t.start()

for t in threads:
    t.join()                   # Wait for all threads to finish

# ── ThreadPoolExecutor ───────────────────────────────
def process_item(item):
    time.sleep(0.1)
    return item ** 2

with concurrent.futures.ThreadPoolExecutor(max_workers=4) as executor:
    results = list(executor.map(process_item, range(20)))
print(results)

# ── Async / Await (modern async) ─────────────────────
async def fetch_data(url):
    await asyncio.sleep(1)     # Simulate async I/O
    return f"Data from {url}"


async def main():
    urls = [f"https://api.example.com/{i}" for i in range(5)]
    tasks = [fetch_data(url) for url in urls]
    results = await asyncio.gather(*tasks)
    for r in results:
        print(r)


asyncio.run(main())
```

---

### 3.3 Regular Expressions

```python
import re

text = "My email is alice@example.com and phone is +91-9876543210"

# ── Pattern Matching ─────────────────────────────────
email_pattern = r"[a-zA-Z0-9_.+-]+@[a-zA-Z0-9-]+\.[a-zA-Z]+"
phone_pattern = r"\+?\d{1,3}[-\s]?\d{10}"

email = re.search(email_pattern, text)
phone = re.search(phone_pattern, text)

print(email.group())           # alice@example.com
print(phone.group())           # +91-9876543210

# ── Find All ─────────────────────────────────────────
numbers = re.findall(r"\d+", "I have 3 cats and 2 dogs")
print(numbers)                 # ['3', '2']

# ── Replace ──────────────────────────────────────────
cleaned = re.sub(r"\s+", " ", "This   has   extra   spaces")
print(cleaned)                 # This has extra spaces

# ── Groups ───────────────────────────────────────────
date_pattern = r"(\d{4})-(\d{2})-(\d{2})"
match = re.search(date_pattern, "Today is 2025-08-15")
if match:
    year, month, day = match.groups()
    print(f"Year: {year}, Month: {month}, Day: {day}")
```

---

### 3.4 Databases

```python
import sqlite3
import json

# ── SQLite3 ──────────────────────────────────────────
conn = sqlite3.connect("school.db")
cursor = conn.cursor()

# Create table
cursor.execute("""
    CREATE TABLE IF NOT EXISTS students (
        id      INTEGER PRIMARY KEY AUTOINCREMENT,
        name    TEXT NOT NULL,
        grade   REAL,
        city    TEXT
    )
""")

# Insert data
students = [
    ("Alice", 92.5, "Delhi"),
    ("Bob",   85.0, "Mumbai"),
    ("Charlie", 78.3, "Chennai")
]
cursor.executemany(
    "INSERT INTO students (name, grade, city) VALUES (?, ?, ?)",
    students
)
conn.commit()

# Query data
cursor.execute("SELECT * FROM students WHERE grade > 80 ORDER BY grade DESC")
rows = cursor.fetchall()
for row in rows:
    print(row)

# Update
cursor.execute("UPDATE students SET grade = 95 WHERE name = 'Alice'")
conn.commit()

# Delete
cursor.execute("DELETE FROM students WHERE city = 'Chennai'")
conn.commit()

conn.close()
```

---

### 3.5 Testing & Debugging

```python
# ── Unit Testing with unittest ───────────────────────
import unittest

def is_palindrome(text):
    clean = text.lower().replace(" ", "")
    return clean == clean[::-1]

def factorial(n):
    if n < 0:
        raise ValueError("n must be non-negative")
    if n == 0:
        return 1
    return n * factorial(n - 1)


class TestFunctions(unittest.TestCase):

    def test_palindrome_true(self):
        self.assertTrue(is_palindrome("racecar"))
        self.assertTrue(is_palindrome("A man a plan a canal Panama"))

    def test_palindrome_false(self):
        self.assertFalse(is_palindrome("hello"))

    def test_factorial_positive(self):
        self.assertEqual(factorial(5), 120)
        self.assertEqual(factorial(0), 1)

    def test_factorial_negative(self):
        with self.assertRaises(ValueError):
            factorial(-1)

    def setUp(self):           # Runs before each test
        pass

    def tearDown(self):        # Runs after each test
        pass


if __name__ == "__main__":
    unittest.main()

# Run: python -m pytest test_functions.py -v
```

---

## 🚀 Module 4 — Expert & Real-World Projects

> **Goal:** Apply Python to build real applications.
> **Duration:** Weeks 10–12 | **Prerequisites:** Module 3

---

### 4.1 Web Development with Flask

```python
from flask import Flask, request, jsonify, render_template
from functools import wraps

app = Flask(__name__)

# In-memory data store
users = {}

# ── Decorator for authentication ─────────────────────
def require_auth(f):
    @wraps(f)
    def decorated(*args, **kwargs):
        token = request.headers.get("Authorization")
        if token != "secret-token":
            return jsonify({"error": "Unauthorized"}), 401
        return f(*args, **kwargs)
    return decorated


# ── Routes ───────────────────────────────────────────
@app.route("/")
def home():
    return "<h1>Welcome to Python API!</h1>"


@app.route("/users", methods=["GET"])
def get_users():
    return jsonify(list(users.values()))


@app.route("/users", methods=["POST"])
def create_user():
    data    = request.get_json()
    user_id = len(users) + 1
    user    = {"id": user_id, **data}
    users[user_id] = user
    return jsonify(user), 201


@app.route("/users/<int:user_id>", methods=["GET"])
@require_auth
def get_user(user_id):
    user = users.get(user_id)
    if not user:
        return jsonify({"error": "User not found"}), 404
    return jsonify(user)


if __name__ == "__main__":
    app.run(debug=True, port=5000)
```

---

### 4.2 Web Scraping

```python
import requests
from bs4 import BeautifulSoup
import pandas as pd
import time

def scrape_quotes():
    base_url  = "http://quotes.toscrape.com"
    all_quotes = []
    page = 1

    while True:
        url = f"{base_url}/page/{page}/"
        response = requests.get(url)

        if response.status_code != 200:
            break

        soup = BeautifulSoup(response.text, "html.parser")
        quotes = soup.select(".quote")

        if not quotes:
            break

        for quote in quotes:
            text   = quote.select_one(".text").text.strip()
            author = quote.select_one(".author").text.strip()
            tags   = [tag.text for tag in quote.select(".tag")]

            all_quotes.append({
                "quote"  : text,
                "author" : author,
                "tags"   : ", ".join(tags)
            })

        print(f"Scraped page {page} — {len(quotes)} quotes")
        page += 1
        time.sleep(1)        # Be respectful!

    df = pd.DataFrame(all_quotes)
    df.to_csv("quotes.csv", index=False)
    print(f"\nTotal quotes: {len(all_quotes)}")
    return df


# df = scrape_quotes()
```

---

### 4.3 Working with APIs

```python
import requests

# ── REST API — GET ────────────────────────────────────
def get_weather(city, api_key):
    url    = "https://api.openweathermap.org/data/2.5/weather"
    params = {"q": city, "appid": api_key, "units": "metric"}

    response = requests.get(url, params=params)
    response.raise_for_status()

    data  = response.json()
    return {
        "city"        : data["name"],
        "temperature" : data["main"]["temp"],
        "humidity"    : data["main"]["humidity"],
        "description" : data["weather"][0]["description"]
    }


# ── REST API — POST ───────────────────────────────────
def create_post(title, body, user_id=1):
    url  = "https://jsonplaceholder.typicode.com/posts"
    data = {"title": title, "body": body, "userId": user_id}

    response = requests.post(url, json=data)
    return response.json()


post = create_post("My First Post", "Python makes APIs easy!")
print(post)
```

---

### 4.4 Automation Scripts

```python
import os
import shutil
from pathlib import Path
from datetime import datetime

def organize_downloads(downloads_path="~/Downloads"):
    """Automatically organize files by type into folders."""
    
    FOLDER_MAP = {
        "Images"    : [".jpg", ".jpeg", ".png", ".gif", ".svg", ".webp"],
        "Documents" : [".pdf", ".docx", ".doc", ".txt", ".xlsx", ".pptx"],
        "Videos"    : [".mp4", ".mkv", ".avi", ".mov"],
        "Audio"     : [".mp3", ".wav", ".flac", ".aac"],
        "Archives"  : [".zip", ".tar", ".gz", ".rar"],
        "Code"      : [".py", ".js", ".html", ".css", ".java", ".cpp"],
    }

    downloads = Path(downloads_path).expanduser()
    moved = 0

    for file in downloads.iterdir():
        if file.is_file():
            ext = file.suffix.lower()
            for folder, extensions in FOLDER_MAP.items():
                if ext in extensions:
                    target_dir = downloads / folder
                    target_dir.mkdir(exist_ok=True)
                    shutil.move(str(file), str(target_dir / file.name))
                    print(f"Moved: {file.name} → {folder}/")
                    moved += 1
                    break

    print(f"\n✅ Organized {moved} files.")


# organize_downloads()
```

---

## Mini Projects by Level

### 🟢 Beginner Projects

| # | Project | Concepts Used |
|---|---|---|
| 1 | Number Guessing Game | loops, conditionals, random |
| 2 | Simple Calculator | functions, input/output |
| 3 | To-Do List (CLI) | lists, file handling |
| 4 | Temperature Converter | functions, math |
| 5 | Password Generator | random, strings |

```python
# ── Project: Number Guessing Game ────────────────────
import random

def guess_game():
    secret = random.randint(1, 100)
    attempts = 0

    print("🎮 Guess the number (1-100)!")

    while True:
        guess = int(input("Your guess: "))
        attempts += 1

        if guess < secret:
            print("📈 Too low!")
        elif guess > secret:
            print("📉 Too high!")
        else:
            print(f"🎉 Correct! You got it in {attempts} attempts!")
            break

guess_game()
```

---

### 🟡 Intermediate Projects

| # | Project | Concepts Used |
|---|---|---|
| 1 | Contact Book App | OOP, file I/O, JSON |
| 2 | Student Grade Manager | OOP, CSV, sorting |
| 3 | ATM Simulator | OOP, exceptions, encapsulation |
| 4 | Quiz Application | OOP, JSON, scoring |
| 5 | Expense Tracker | OOP, CSV, aggregation |

---

### 🔴 Advanced Projects

| # | Project | Concepts Used |
|---|---|---|
| 1 | REST API Server | Flask, SQLite, JSON |
| 2 | Web Scraper + Dashboard | BeautifulSoup, Pandas, Plotly |
| 3 | Chat Application | Sockets, threading |
| 4 | File Organizer | os, shutil, automation |
| 5 | Personal Finance Tracker | SQLite, OOP, Matplotlib |

---

## Cheat Sheets

### String Methods
```python
s = "Hello, Python!"
s.upper()         # HELLO, PYTHON!
s.lower()         # hello, python!
s.strip()         # Remove whitespace
s.split(", ")     # ['Hello', 'Python!']
", ".join(["a", "b", "c"])  # a, b, c
s.replace("Python", "World")
s.startswith("Hello")       # True
s.endswith("!")             # True
s.find("Python")            # 7
s.count("l")                # 3
s.isdigit()                 # False
s.isalpha()                 # False
```

### List Methods
```python
lst = [3, 1, 4, 1, 5]
lst.append(9)       # Add to end
lst.insert(0, 0)    # Insert at index
lst.remove(1)       # Remove first occurrence
lst.pop()           # Remove & return last
lst.pop(0)          # Remove at index
lst.sort()          # In-place sort
lst.reverse()       # In-place reverse
lst.index(4)        # Find index
lst.count(1)        # Count occurrences
lst.clear()         # Remove all
lst2 = lst.copy()   # Shallow copy
```

### Dictionary Methods
```python
d = {"a": 1, "b": 2}
d.get("c", 0)       # 0  (safe get)
d.keys()            # dict_keys
d.values()          # dict_values
d.items()           # dict_items
d.update({"c": 3})  # Merge
d.pop("a")          # Remove & return
d.setdefault("d", 4)# Set if missing
d.copy()            # Shallow copy
```

### Common Built-ins
```python
len([1,2,3])        # 3
range(1, 10, 2)     # 1,3,5,7,9
enumerate(["a","b"]) # (0,'a'), (1,'b')
zip([1,2], [3,4])   # (1,3), (2,4)
map(str, [1,2,3])   # ['1','2','3']
filter(lambda x: x>2, [1,2,3,4])  # [3,4]
sorted([3,1,2])     # [1,2,3]
reversed([1,2,3])   # 3,2,1
sum([1,2,3])        # 6
min([3,1,2])        # 1
max([3,1,2])        # 3
abs(-5)             # 5
round(3.14159, 2)   # 3.14
isinstance(5, int)  # True
```

---

## Learning Resources

### 📚 Official Documentation
- [Python Official Docs](https://docs.python.org/3/)
- [Python Standard Library](https://docs.python.org/3/library/)
- [PEP 8 Style Guide](https://pep8.org/)

### 🎓 Free Learning Platforms
- [Kaggle Learn](https://www.kaggle.com/learn/python) — Free Python course with exercises
- [freeCodeCamp](https://www.freecodecamp.org/) — Python certifications
- [Codecademy](https://www.codecademy.com/learn/learn-python-3) — Interactive lessons
- [Real Python](https://realpython.com/) — Tutorials and articles

### 📖 Recommended Books
| Book | Author | Level |
|---|---|---|
| *Automate the Boring Stuff with Python* | Al Sweigart | Beginner |
| *Python Crash Course* | Eric Matthes | Beginner |
| *Fluent Python* | Luciano Ramalho | Advanced |
| *Clean Code in Python* | Mariano Anaya | Advanced |
| *Python Cookbook* | David Beazley | Advanced |

### 🏆 Practice & Challenges
- [LeetCode](https://leetcode.com/) — Coding challenges
- [HackerRank](https://www.hackerrank.com/domains/python) — Python challenges
- [Codewars](https://www.codewars.com/) — Kata style problems
- [Project Euler](https://projecteuler.net/) — Math + programming

### 🎥 YouTube Channels
- Corey Schafer — In-depth Python tutorials
- Tech With Tim — Projects and tutorials
- Sentdex — Python for AI/Data
- CS Dojo — Algorithms and Python

---

## Recommended Learning Path

```
Week 1–2   →  Syntax, Variables, Loops, Functions
Week 3     →  Data Structures (lists, dicts, sets)
Week 4     →  OOP — Classes, Inheritance
Week 5     →  File I/O, Exceptions, JSON/CSV
Week 6     →  Modules, APIs, Web Scraping Basics
Week 7     →  Decorators, Generators, Advanced OOP
Week 8     →  Databases, Testing
Week 9     →  Concurrency, Regex, Performance
Week 10    →  Flask / Web Development
Week 11    →  Automation & Scripting
Week 12    →  Capstone Project
```

---

## Contributing

Contributions are always welcome! 🙌

1. Fork this repository
2. Create a feature branch: `git checkout -b feature/add-new-topic`
3. Commit your changes: `git commit -m "Add: New topic on decorators"`
4. Push to the branch: `git push origin feature/add-new-topic`
5. Open a Pull Request

Please follow the [PEP 8](https://pep8.org/) style guide for all Python code contributions.

---

## License

This project is licensed under the **MIT License** — see the [LICENSE](LICENSE) file for details.

---

<div align="center">

**Made with ❤️ for Python Learners Everywhere**

If this helped you, consider giving it a ⭐ on GitHub!

*"The journey of a thousand miles begins with a single `print('Hello, World!')`"*

</div>
