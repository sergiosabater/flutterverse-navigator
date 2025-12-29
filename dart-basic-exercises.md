<div align="center">

# 🎯 Dart Basic Exercises 💪

### *Practice makes perfect: Master Dart through hands-on coding*

[![Dart Version](https://img.shields.io/badge/Dart-%3E%3D%203.0-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
[![Difficulty](https://img.shields.io/badge/Difficulty-Beginner%20to%20Intermediate-success?style=for-the-badge)](https://dartpad.dev/)
[![Practice](https://img.shields.io/badge/Practice-DartPad-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dartpad.dev/)

**Learn by doing. Code by practicing. Master by repeating.**

---

</div>

## 🎓 How to Use This Guide

1. 📖 **Read the exercise description carefully**
2. 💭 **Think about the solution before coding**
3. 💻 **Write your code in [DartPad](https://dartpad.dev/)**
4. ✅ **Test with different inputs**
5. 🔍 **Check the solution if you get stuck**
6. 🚀 **Try to solve it differently**

```dart
// Your practice workflow
void main() {
  readExercise();
  thinkAboutSolution();
  writeCode();
  test();
  improve();
}
```

---

## 📊 Exercise Levels

<div align="center">

| 🎯 Level | 📝 Description | 🔢 Exercises |
|:---:|:---|:---:|
| 🟢 **Beginner** | Variables, operators, basic functions | 1-15 |
| 🟡 **Elementary** | Collections, control flow, strings | 16-30 |
| 🟠 **Intermediate** | OOP, functions, algorithms | 31-45 |
| 🔴 **Advanced** | Async, generics, advanced patterns | 46-50 |

</div>

---

## 🟢 Level 1: Beginner (1-15)

<div align="center">

### Variables, Types & Basic Operations

</div>

<table>
<tr>
<td width="50%" valign="top">

### 📝 Exercise 1: Hello World
**Difficulty:** ⭐

Create a program that prints "Hello, Dart!" to the console.

```dart
void main() {
  // Your code here
}
```

**Expected Output:**
```
Hello, Dart!
```

<details>
<summary>💡 Hint</summary>

Use the `print()` function!
</details>

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  print('Hello, Dart!');
}
```
</details>

---

### 📝 Exercise 2: Variable Declaration
**Difficulty:** ⭐

Declare variables for your name (String), age (int), and height in meters (double). Print them.

**Expected Output:**
```
Name: John
Age: 25
Height: 1.75
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  String name = 'John';
  int age = 25;
  double height = 1.75;
  
  print('Name: $name');
  print('Age: $age');
  print('Height: $height');
}
```
</details>

---

### 📝 Exercise 3: Simple Calculator
**Difficulty:** ⭐

Create variables for two numbers and print their sum, difference, product, and division.

**Expected Output:**
```
10 + 5 = 15
10 - 5 = 5
10 * 5 = 50
10 / 5 = 2.0
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  int a = 10;
  int b = 5;
  
  print('$a + $b = ${a + b}');
  print('$a - $b = ${a - b}');
  print('$a * $b = ${a * b}');
  print('$a / $b = ${a / b}');
}
```
</details>

</td>
<td width="50%" valign="top">

### 📝 Exercise 4: Type Conversion
**Difficulty:** ⭐

Convert a string "123" to an integer and "45.67" to a double, then add them.

**Expected Output:**
```
Result: 168.67
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  String numStr = '123';
  String doubleStr = '45.67';
  
  int num = int.parse(numStr);
  double dec = double.parse(doubleStr);
  
  print('Result: ${num + dec}');
}
```
</details>

---

### 📝 Exercise 5: Even or Odd
**Difficulty:** ⭐⭐

Write a function that checks if a number is even or odd.

**Expected Output:**
```
7 is odd
10 is even
```

<details>
<summary>💡 Hint</summary>

Use the modulo operator `%`
</details>

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  checkEvenOdd(7);
  checkEvenOdd(10);
}

void checkEvenOdd(int number) {
  if (number % 2 == 0) {
    print('$number is even');
  } else {
    print('$number is odd');
  }
}
```
</details>

---

### 📝 Exercise 6: Maximum of Two
**Difficulty:** ⭐⭐

Create a function that returns the larger of two numbers.

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  print(max(15, 20)); // 20
  print(max(100, 50)); // 100
}

int max(int a, int b) {
  return a > b ? a : b;
}
```
</details>

</td>
</tr>
</table>

### 📝 Exercise 7-15: Quick Challenges

<div align="center">

| # | 🎯 Challenge | 💪 Difficulty |
|:---:|:---|:---:|
| **7** | Calculate the area of a rectangle (width × height) | ⭐ |
| **8** | Convert Celsius to Fahrenheit: `F = C × 9/5 + 32` | ⭐ |
| **9** | Check if a number is positive, negative, or zero | ⭐⭐ |
| **10** | Calculate the average of three numbers | ⭐ |
| **11** | Check if a year is a leap year | ⭐⭐ |
| **12** | Find the absolute value of a number | ⭐ |
| **13** | Calculate simple interest: `(P × R × T) / 100` | ⭐ |
| **14** | Swap two variables without a third variable | ⭐⭐ |
| **15** | Calculate the perimeter of a circle: `2πr` | ⭐ |

</div>

---

## 🟡 Level 2: Elementary (16-30)

<div align="center">

### Collections, Loops & Strings

</div>

<table>
<tr>
<td width="50%" valign="top">

### 📝 Exercise 16: List Sum
**Difficulty:** ⭐⭐

Calculate the sum of all numbers in a list.

```dart
void main() {
  List<int> numbers = [1, 2, 3, 4, 5];
  // Your code here
}
```

**Expected Output:**
```
Sum: 15
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  List<int> numbers = [1, 2, 3, 4, 5];
  int sum = 0;
  
  for (int num in numbers) {
    sum += num;
  }
  
  print('Sum: $sum');
  
  // Alternative using reduce
  int sum2 = numbers.reduce((a, b) => a + b);
  print('Sum: $sum2');
}
```
</details>

---

### 📝 Exercise 17: Find Maximum in List
**Difficulty:** ⭐⭐

Find the largest number in a list.

**Expected Output:**
```
Maximum: 89
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  List<int> numbers = [23, 89, 12, 45, 67];
  int max = numbers[0];
  
  for (int num in numbers) {
    if (num > max) {
      max = num;
    }
  }
  
  print('Maximum: $max');
  
  // Alternative
  print('Maximum: ${numbers.reduce((a, b) => a > b ? a : b)}');
}
```
</details>

---

### 📝 Exercise 18: Reverse a String
**Difficulty:** ⭐⭐

Reverse the characters in a string.

**Expected Output:**
```
Original: Dart
Reversed: traD
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  String original = 'Dart';
  String reversed = original.split('').reversed.join('');
  
  print('Original: $original');
  print('Reversed: $reversed');
}
```
</details>

</td>
<td width="50%" valign="top">

### 📝 Exercise 19: Count Vowels
**Difficulty:** ⭐⭐

Count the number of vowels in a string.

**Expected Output:**
```
Vowels in "Hello World": 3
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  String text = 'Hello World';
  int count = countVowels(text);
  print('Vowels in "$text": $count');
}

int countVowels(String text) {
  int count = 0;
  String vowels = 'aeiouAEIOU';
  
  for (int i = 0; i < text.length; i++) {
    if (vowels.contains(text[i])) {
      count++;
    }
  }
  
  return count;
}
```
</details>

---

### 📝 Exercise 20: Palindrome Check
**Difficulty:** ⭐⭐

Check if a string is a palindrome (reads the same forwards and backwards).

**Expected Output:**
```
"radar" is a palindrome
"hello" is not a palindrome
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  checkPalindrome('radar');
  checkPalindrome('hello');
}

void checkPalindrome(String text) {
  String reversed = text.split('').reversed.join('');
  
  if (text.toLowerCase() == reversed.toLowerCase()) {
    print('"$text" is a palindrome');
  } else {
    print('"$text" is not a palindrome');
  }
}
```
</details>

---

### 📝 Exercise 21: Factorial
**Difficulty:** ⭐⭐

Calculate the factorial of a number (n! = n × (n-1) × ... × 1).

**Expected Output:**
```
Factorial of 5: 120
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  print('Factorial of 5: ${factorial(5)}');
}

int factorial(int n) {
  if (n <= 1) return 1;
  return n * factorial(n - 1);
  
  // Iterative approach
  // int result = 1;
  // for (int i = 2; i <= n; i++) {
  //   result *= i;
  // }
  // return result;
}
```
</details>

</td>
</tr>
</table>

### 📝 Exercise 22-30: Quick Challenges

<div align="center">

| # | 🎯 Challenge | 💪 Difficulty |
|:---:|:---|:---:|
| **22** | Print multiplication table for a given number | ⭐⭐ |
| **23** | Count the occurrences of a character in a string | ⭐⭐ |
| **24** | Remove duplicates from a list | ⭐⭐⭐ |
| **25** | Find prime numbers up to N | ⭐⭐⭐ |
| **26** | Calculate Fibonacci sequence up to N terms | ⭐⭐ |
| **27** | Sort a list of numbers (bubble sort) | ⭐⭐⭐ |
| **28** | Check if a string contains only digits | ⭐⭐ |
| **29** | Flatten a nested list | ⭐⭐⭐ |
| **30** | Find the second largest number in a list | ⭐⭐⭐ |

</div>

---

## 🟠 Level 3: Intermediate (31-45)

<div align="center">

### Object-Oriented Programming & Advanced Functions

</div>

<table>
<tr>
<td width="50%" valign="top">

### 📝 Exercise 31: Create a Person Class
**Difficulty:** ⭐⭐

Create a `Person` class with name and age properties, and a method to introduce themselves.

**Expected Output:**
```
Hi, I'm John and I'm 25 years old
Hi, I'm Alice and I'm 30 years old
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  Person person1 = Person('John', 25);
  Person person2 = Person('Alice', 30);
  
  person1.introduce();
  person2.introduce();
}

class Person {
  String name;
  int age;
  
  Person(this.name, this.age);
  
  void introduce() {
    print("Hi, I'm $name and I'm $age years old");
  }
}
```
</details>

---

### 📝 Exercise 32: Bank Account
**Difficulty:** ⭐⭐⭐

Create a `BankAccount` class with deposit and withdraw methods.

**Expected Output:**
```
Deposited: $500.0
Current balance: $500.0
Withdrawn: $200.0
Current balance: $300.0
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  BankAccount account = BankAccount('John Doe');
  account.deposit(500);
  account.withdraw(200);
}

class BankAccount {
  String owner;
  double _balance = 0;
  
  BankAccount(this.owner);
  
  double get balance => _balance;
  
  void deposit(double amount) {
    if (amount > 0) {
      _balance += amount;
      print('Deposited: \$$amount');
      print('Current balance: \$$_balance');
    }
  }
  
  void withdraw(double amount) {
    if (amount > 0 && amount <= _balance) {
      _balance -= amount;
      print('Withdrawn: \$$amount');
      print('Current balance: \$$_balance');
    } else {
      print('Insufficient funds');
    }
  }
}
```
</details>

</td>
<td width="50%" valign="top">

### 📝 Exercise 33: Rectangle Class
**Difficulty:** ⭐⭐

Create a `Rectangle` class with getters for area and perimeter.

**Expected Output:**
```
Area: 50
Perimeter: 30
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  Rectangle rect = Rectangle(10, 5);
  print('Area: ${rect.area}');
  print('Perimeter: ${rect.perimeter}');
}

class Rectangle {
  double width;
  double height;
  
  Rectangle(this.width, this.height);
  
  double get area => width * height;
  double get perimeter => 2 * (width + height);
}
```
</details>

---

### 📝 Exercise 34: Animal Inheritance
**Difficulty:** ⭐⭐⭐

Create an `Animal` base class and `Dog` and `Cat` subclasses with different sounds.

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  Dog dog = Dog('Buddy');
  Cat cat = Cat('Whiskers');
  
  dog.makeSound();
  cat.makeSound();
}

abstract class Animal {
  String name;
  Animal(this.name);
  
  void makeSound();
}

class Dog extends Animal {
  Dog(String name) : super(name);
  
  @override
  void makeSound() {
    print('$name says: Woof!');
  }
}

class Cat extends Animal {
  Cat(String name) : super(name);
  
  @override
  void makeSound() {
    print('$name says: Meow!');
  }
}
```
</details>

---

### 📝 Exercise 35: Shopping Cart
**Difficulty:** ⭐⭐⭐

Create a shopping cart system with items and total calculation.

<details>
<summary>💡 Hint</summary>

Use a Map to store items and quantities!
</details>

</td>
</tr>
</table>

### 📝 Exercise 36-45: OOP Challenges

<div align="center">

| # | 🎯 Challenge | 💪 Difficulty |
|:---:|:---|:---:|
| **36** | Create a `Book` class with title, author, and pages | ⭐⭐ |
| **37** | Implement a `Student` class with grades and average calculation | ⭐⭐ |
| **38** | Create a `Calculator` class with static methods | ⭐⭐ |
| **39** | Implement a simple `Stack` data structure | ⭐⭐⭐ |
| **40** | Create a `Queue` data structure | ⭐⭐⭐ |
| **41** | Build a `TodoList` class with add/remove/complete methods | ⭐⭐⭐ |
| **42** | Implement a `Temperature` class with Celsius/Fahrenheit conversion | ⭐⭐ |
| **43** | Create a `Counter` class using factory constructor | ⭐⭐⭐ |
| **44** | Build a `Logger` singleton class | ⭐⭐⭐ |
| **45** | Implement a simple `LinkedList` | ⭐⭐⭐⭐ |

</div>

---

## 🔴 Level 4: Advanced (46-50)

<div align="center">

### Async, Generics & Advanced Patterns

</div>

<table>
<tr>
<td width="50%" valign="top">

### 📝 Exercise 46: Async Data Fetching
**Difficulty:** ⭐⭐⭐

Simulate fetching data with a delay using `Future`.

```dart
void main() async {
  print('Fetching data...');
  // Your code here
}
```

**Expected Output:**
```
Fetching data...
Data received: User Data
```

<details>
<summary>✅ Solution</summary>

```dart
void main() async {
  print('Fetching data...');
  String data = await fetchData();
  print('Data received: $data');
}

Future<String> fetchData() async {
  await Future.delayed(Duration(seconds: 2));
  return 'User Data';
}
```
</details>

---

### 📝 Exercise 47: Generic Box
**Difficulty:** ⭐⭐⭐

Create a generic `Box<T>` class that can hold any type.

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  Box<int> intBox = Box(42);
  Box<String> stringBox = Box('Hello');
  
  print(intBox.getValue()); // 42
  print(stringBox.getValue()); // Hello
}

class Box<T> {
  T _value;
  
  Box(this._value);
  
  T getValue() => _value;
  void setValue(T value) => _value = value;
}
```
</details>

</td>
<td width="50%" valign="top">

### 📝 Exercise 48: Stream Counter
**Difficulty:** ⭐⭐⭐⭐

Create a stream that emits numbers every second.

<details>
<summary>✅ Solution</summary>

```dart
void main() async {
  await for (int value in countStream(5)) {
    print('Count: $value');
  }
}

Stream<int> countStream(int max) async* {
  for (int i = 1; i <= max; i++) {
    await Future.delayed(Duration(seconds: 1));
    yield i;
  }
}
```
</details>

---

### 📝 Exercise 49: Extension Methods
**Difficulty:** ⭐⭐⭐

Add custom methods to the `String` class using extensions.

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  print('dart'.capitalize()); // Dart
  print('hello@email.com'.isEmail); // true
}

extension StringExtension on String {
  String capitalize() {
    if (isEmpty) return this;
    return '${this[0].toUpperCase()}${substring(1)}';
  }
  
  bool get isEmail => contains('@') && contains('.');
}
```
</details>

---

### 📝 Exercise 50: Future Error Handling
**Difficulty:** ⭐⭐⭐

Handle errors in asynchronous operations properly.

<details>
<summary>✅ Solution</summary>

```dart
void main() async {
  try {
    String result = await riskyOperation();
    print('Success: $result');
  } catch (e) {
    print('Error: $e');
  }
}

Future<String> riskyOperation() async {
  await Future.delayed(Duration(seconds: 1));
  throw Exception('Something went wrong!');
}
```
</details>

</td>
</tr>
</table>

---

## 🎯 Practice Projects

<div align="center">

### Put Your Skills Together! 🚀

</div>

### 🏆 Project 1: Contact Book
**Level:** Intermediate  
**Topics:** OOP, Lists, Maps

Create a contact book application that can:
- Add new contacts (name, phone, email)
- Search contacts by name
- Delete contacts
- Display all contacts

---

### 🏆 Project 2: To-Do List Manager
**Level:** Intermediate  
**Topics:** OOP, Collections, State Management

Build a to-do list with:
- Add tasks
- Mark tasks as complete
- Delete tasks
- Filter by status (all, active, completed)
- Save/load from "storage" (List)

---

### 🏆 Project 3: Simple Calculator
**Level:** Elementary  
**Topics:** Functions, Control Flow

Create a calculator that:
- Performs basic operations (+, -, *, /)
- Shows operation history
- Handles division by zero

---

### 🏆 Project 4: Quiz Game
**Level:** Intermediate  
**Topics:** OOP, Collections, Logic

Build a quiz game with:
- Multiple choice questions
- Score tracking
- Question randomization
- Results summary

---

### 🏆 Project 5: Weather Data Simulator
**Level:** Advanced  
**Topics:** Async, Streams, OOP

Simulate weather data:
- Generate random temperatures
- Stream data every few seconds
- Calculate averages
- Detect extreme temperatures

---

## 📚 Additional Resources

<div align="center">

### 🎓 Keep Learning!

[![DartPad](https://img.shields.io/badge/Practice-DartPad-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dartpad.dev/)
[![Exercism](https://img.shields.io/badge/Exercism-Dart%20Track-009CAB?style=for-the-badge)](https://exercism.org/tracks/dart)
[![Codewars](https://img.shields.io/badge/Codewars-Dart%20Challenges-B1361E?style=for-the-badge)](https://www.codewars.com/)
[![LeetCode](https://img.shields.io/badge/LeetCode-Practice-FFA116?style=for-the-badge)](https://leetcode.com/)

</div>

#### 🌟 More Practice
- 🎮 [Exercism Dart Track](https://exercism.org/tracks/dart) - Mentored practice
- 💪 [Codewars](https://www.codewars.com/) - Coding challenges
- 📖 [Dart Cookbook](https://docs.flutter.dev/cookbook) - Practical recipes
- 🎯 [HackerRank](https://www.hackerrank.com/) - Algorithmic challenges
- 📝 [Project Euler](https://projecteuler.net/) - Mathematical problems

---

## 💡 Tips for Success

```
┌──────────────────────────────────────────────┐
│  ✅ Practice every day (consistency > time)  │
│  ✅ Start simple, gradually increase         │
│  ✅ Don't look at solutions immediately      │
│  ✅ Try multiple approaches                  │
│  ✅ Refactor and improve your code           │
│  ✅ Share and discuss with others            │
│  ✅ Build real projects                      │
└──────────────────────────────────────────────┘
```

---

<div align="center">

### 💙 *"Learning to write programs stretches your mind, and helps you think better."* – Bill Gates

**Keep Coding, Keep Growing! 🎯✨**

---

Made with 💙 by the Dart community

[⬆ Back to top](#-dart-basic-exercises-)

</div>
