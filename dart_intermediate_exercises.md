<div align="center">

# 🎯 Dart Intermediate Exercises 🚀

### *Level up your Dart skills: From competent to confident*

[![Dart Version](https://img.shields.io/badge/Dart-%3E%3D%203.0-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
[![Difficulty](https://img.shields.io/badge/Difficulty-Intermediate%20to%20Advanced-orange?style=for-the-badge)](https://dartpad.dev/)
[![Practice](https://img.shields.io/badge/Practice-DartPad-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dartpad.dev/)

**Master advanced Dart concepts through challenging exercises**  
`Functional Programming` • `Advanced OOP` • `Async Patterns` • `Design Patterns` • `Algorithms`

---

</div>

## 🎓 Prerequisites

Before starting these exercises, you should be comfortable with:

<div align="center">

| ✅ Skill | 📝 Description |
|:---:|:---|
| **Basic Syntax** | Variables, functions, control flow |
| **OOP Fundamentals** | Classes, inheritance, interfaces |
| **Collections** | Lists, Maps, Sets and their methods |
| **Basic Async** | Future, async/await basics |
| **Problem Solving** | Algorithmic thinking |

</div>

```dart
// If you can understand this, you're ready!
void main() async {
  final numbers = [1, 2, 3, 4, 5];
  final squared = numbers.map((n) => n * n).toList();
  
  final result = await Future.delayed(
    Duration(seconds: 1),
    () => squared.reduce((a, b) => a + b),
  );
  
  print('Sum of squares: $result'); // 55
}
```

---

## 📊 Exercise Categories

```
┌─────────────────────────────────────────┐
│  🎨 Functional Programming (1-10)       │
│  🏗️  Advanced OOP (11-20)               │
│  ⚡ Async & Concurrency (21-30)         │
│  🎯 Design Patterns (31-40)             │
│  🧮 Algorithms & Data Structures (41-50)│
│  🔥 Challenge Projects (Bonus)          │
└─────────────────────────────────────────┘
```

---

## 🎨 Section 1: Functional Programming (1-10)

<div align="center">

### Master Higher-Order Functions & Functional Patterns

</div>

<table>
<tr>
<td width="50%" valign="top">

### 📝 Exercise 1: Custom Map Function
**Difficulty:** ⭐⭐⭐

Implement your own version of the `map` function without using the built-in method.

```dart
void main() {
  List<int> numbers = [1, 2, 3, 4, 5];
  List<int> doubled = customMap(numbers, (n) => n * 2);
  print(doubled); // [2, 4, 6, 8, 10]
}

List<T> customMap<T, S>(List<S> list, T Function(S) fn) {
  // Your implementation
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  List<int> numbers = [1, 2, 3, 4, 5];
  List<int> doubled = customMap(numbers, (n) => n * 2);
  print(doubled); // [2, 4, 6, 8, 10]
}

List<T> customMap<T, S>(List<S> list, T Function(S) fn) {
  List<T> result = [];
  for (var item in list) {
    result.add(fn(item));
  }
  return result;
}
```
</details>

---

### 📝 Exercise 2: Function Composition
**Difficulty:** ⭐⭐⭐

Create a function that composes two functions together.

```dart
void main() {
  var addTwo = (int x) => x + 2;
  var multiplyByThree = (int x) => x * 3;
  
  var composed = compose(multiplyByThree, addTwo);
  print(composed(5)); // (5 + 2) * 3 = 21
}

Function compose(Function f, Function g) {
  // Your implementation
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  var addTwo = (int x) => x + 2;
  var multiplyByThree = (int x) => x * 3;
  
  var composed = compose(multiplyByThree, addTwo);
  print(composed(5)); // 21
}

Function compose(Function f, Function g) {
  return (x) => f(g(x));
}
```
</details>

---

### 📝 Exercise 3: Curry Function
**Difficulty:** ⭐⭐⭐⭐

Implement currying for a function that takes three parameters.

```dart
void main() {
  var add = curry((a, b, c) => a + b + c);
  print(add(1)(2)(3)); // 6
  
  var addFive = add(5);
  print(addFive(10)(15)); // 30
}
```

<details>
<summary>💡 Hint</summary>

Return nested functions that capture parameters!
</details>

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  var add = curry((a, b, c) => a + b + c);
  print(add(1)(2)(3)); // 6
  
  var addFive = add(5);
  print(addFive(10)(15)); // 30
}

Function curry(Function fn) {
  return (a) => (b) => (c) => fn(a, b, c);
}
```
</details>

</td>
<td width="50%" valign="top">

### 📝 Exercise 4: Memoization
**Difficulty:** ⭐⭐⭐⭐

Create a memoization wrapper that caches function results.

```dart
void main() {
  var fibonacci = memoize((int n) {
    print('Calculating fib($n)');
    if (n <= 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
  });
  
  print(fibonacci(5)); // Calculates
  print(fibonacci(5)); // Uses cache
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  var fibonacci = memoize((int n) {
    print('Calculating fib($n)');
    if (n <= 1) return n;
    return fibonacci(n - 1) + fibonacci(n - 2);
  });
  
  print(fibonacci(5));
  print(fibonacci(5)); // Cached
}

Function memoize(Function fn) {
  Map<dynamic, dynamic> cache = {};
  
  return (arg) {
    if (cache.containsKey(arg)) {
      print('Using cache for $arg');
      return cache[arg];
    }
    
    var result = fn(arg);
    cache[arg] = result;
    return result;
  };
}
```
</details>

---

### 📝 Exercise 5: Partial Application
**Difficulty:** ⭐⭐⭐

Implement partial application for functions.

```dart
void main() {
  int multiply(int a, int b, int c) => a * b * c;
  
  var double = partial(multiply, 2);
  print(double(3, 4)); // 2 * 3 * 4 = 24
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  int multiply(int a, int b, int c) => a * b * c;
  
  var doubleIt = partial(multiply, 2);
  print(doubleIt(3, 4)); // 24
}

Function partial(Function fn, dynamic arg1) {
  return (arg2, arg3) => fn(arg1, arg2, arg3);
}
```
</details>

---

### 📝 Exercise 6: Lazy Evaluation
**Difficulty:** ⭐⭐⭐⭐

Create a lazy list that only computes values when needed.

<details>
<summary>💡 Hint</summary>

Use `Iterable` and generators!
</details>

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  var lazyNumbers = lazyRange(1, 1000000);
  
  // Only computes first 5
  print(lazyNumbers.take(5).toList()); // [1, 2, 3, 4, 5]
}

Iterable<int> lazyRange(int start, int end) sync* {
  for (int i = start; i <= end; i++) {
    print('Generating $i');
    yield i;
  }
}
```
</details>

</td>
</tr>
</table>

### 📝 Exercise 7-10: Functional Challenges

<div align="center">

| # | 🎯 Challenge | 💪 Difficulty |
|:---:|:---|:---:|
| **7** | Implement a custom `filter` function using generics | ⭐⭐⭐ |
| **8** | Create a `pipe` function (reverse of compose) | ⭐⭐⭐ |
| **9** | Build a `debounce` function with timing control | ⭐⭐⭐⭐ |
| **10** | Implement `flatMap` for nested lists | ⭐⭐⭐ |

</div>

---

## 🏗️ Section 2: Advanced OOP (11-20)

<div align="center">

### Mixins, Abstract Classes & Advanced Patterns

</div>

<table>
<tr>
<td width="50%" valign="top">

### 📝 Exercise 11: Mixins for Behaviors
**Difficulty:** ⭐⭐⭐

Create reusable mixins for common behaviors.

```dart
void main() {
  var dog = Dog('Buddy');
  dog.walk();
  dog.swim();
  dog.eat();
}

// Define Walking, Swimming, and Eating mixins
// Apply them to Animal classes
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  var dog = Dog('Buddy');
  dog.walk();
  dog.swim();
  dog.eat();
  
  var fish = Fish('Nemo');
  fish.swim();
  fish.eat();
  // fish.walk(); // Error: Fish can't walk
}

mixin Walking {
  void walk() => print('Walking on land');
}

mixin Swimming {
  void swim() => print('Swimming in water');
}

mixin Eating {
  void eat() => print('Eating food');
}

abstract class Animal {
  String name;
  Animal(this.name);
}

class Dog extends Animal with Walking, Swimming, Eating {
  Dog(String name) : super(name);
}

class Fish extends Animal with Swimming, Eating {
  Fish(String name) : super(name);
}
```
</details>

---

### 📝 Exercise 12: Factory Pattern
**Difficulty:** ⭐⭐⭐

Implement a factory constructor for different shapes.

```dart
void main() {
  Shape circle = Shape.circle(5);
  Shape rectangle = Shape.rectangle(4, 6);
  
  print(circle.area());
  print(rectangle.area());
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  Shape circle = Shape.circle(5);
  Shape rectangle = Shape.rectangle(4, 6);
  
  print('Circle area: ${circle.area()}');
  print('Rectangle area: ${rectangle.area()}');
}

abstract class Shape {
  double area();
  
  factory Shape.circle(double radius) {
    return Circle(radius);
  }
  
  factory Shape.rectangle(double width, double height) {
    return Rectangle(width, height);
  }
}

class Circle implements Shape {
  final double radius;
  Circle(this.radius);
  
  @override
  double area() => 3.14159 * radius * radius;
}

class Rectangle implements Shape {
  final double width, height;
  Rectangle(this.width, this.height);
  
  @override
  double area() => width * height;
}
```
</details>

</td>
<td width="50%" valign="top">

### 📝 Exercise 13: Singleton Pattern
**Difficulty:** ⭐⭐⭐

Create a proper singleton with factory constructor.

```dart
void main() {
  var db1 = Database();
  var db2 = Database();
  
  print(identical(db1, db2)); // true
  
  db1.connect();
  db2.query('SELECT * FROM users');
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  var db1 = Database();
  var db2 = Database();
  
  print(identical(db1, db2)); // true
  
  db1.connect();
  db2.query('SELECT * FROM users');
}

class Database {
  static final Database _instance = Database._internal();
  
  factory Database() {
    return _instance;
  }
  
  Database._internal();
  
  void connect() {
    print('Connected to database');
  }
  
  void query(String sql) {
    print('Executing: $sql');
  }
}
```
</details>

---

### 📝 Exercise 14: Builder Pattern
**Difficulty:** ⭐⭐⭐⭐

Implement a fluent builder for complex objects.

```dart
void main() {
  var user = UserBuilder()
    .setName('John')
    .setAge(30)
    .setEmail('john@example.com')
    .addHobby('Reading')
    .addHobby('Gaming')
    .build();
    
  print(user);
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  var user = UserBuilder()
    .setName('John')
    .setAge(30)
    .setEmail('john@example.com')
    .addHobby('Reading')
    .addHobby('Gaming')
    .build();
    
  print(user);
}

class User {
  final String name;
  final int age;
  final String email;
  final List<String> hobbies;
  
  User(this.name, this.age, this.email, this.hobbies);
  
  @override
  String toString() => 
    'User: $name, $age, $email, Hobbies: $hobbies';
}

class UserBuilder {
  String? _name;
  int? _age;
  String? _email;
  List<String> _hobbies = [];
  
  UserBuilder setName(String name) {
    _name = name;
    return this;
  }
  
  UserBuilder setAge(int age) {
    _age = age;
    return this;
  }
  
  UserBuilder setEmail(String email) {
    _email = email;
    return this;
  }
  
  UserBuilder addHobby(String hobby) {
    _hobbies.add(hobby);
    return this;
  }
  
  User build() {
    return User(_name!, _age!, _email!, _hobbies);
  }
}
```
</details>

</td>
</tr>
</table>

### 📝 Exercise 15-20: OOP Challenges

<div align="center">

| # | 🎯 Challenge | 💪 Difficulty |
|:---:|:---|:---:|
| **15** | Implement Observer pattern for event handling | ⭐⭐⭐⭐ |
| **16** | Create a Strategy pattern for different algorithms | ⭐⭐⭐ |
| **17** | Build a decorator pattern for adding features | ⭐⭐⭐⭐ |
| **18** | Implement Command pattern for undo/redo | ⭐⭐⭐⭐⭐ |
| **19** | Create an Adapter pattern for incompatible interfaces | ⭐⭐⭐ |
| **20** | Build a Composite pattern for tree structures | ⭐⭐⭐⭐ |

</div>

---

## ⚡ Section 3: Async & Concurrency (21-30)

<div align="center">

### Master Asynchronous Programming

</div>

<table>
<tr>
<td width="50%" valign="top">

### 📝 Exercise 21: Parallel Futures
**Difficulty:** ⭐⭐⭐

Execute multiple async operations in parallel.

```dart
void main() async {
  // Fetch user, posts, and comments in parallel
  // Calculate total time taken
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() async {
  final stopwatch = Stopwatch()..start();
  
  final results = await Future.wait([
    fetchUser(),
    fetchPosts(),
    fetchComments(),
  ]);
  
  stopwatch.stop();
  
  print('User: ${results[0]}');
  print('Posts: ${results[1]}');
  print('Comments: ${results[2]}');
  print('Time: ${stopwatch.elapsedMilliseconds}ms');
}

Future<String> fetchUser() async {
  await Future.delayed(Duration(seconds: 1));
  return 'User Data';
}

Future<String> fetchPosts() async {
  await Future.delayed(Duration(seconds: 2));
  return 'Posts Data';
}

Future<String> fetchComments() async {
  await Future.delayed(Duration(seconds: 1));
  return 'Comments Data';
}
```
</details>

---

### 📝 Exercise 22: Stream Transformations
**Difficulty:** ⭐⭐⭐⭐

Transform and filter a stream of events.

```dart
void main() async {
  // Create a stream of numbers
  // Filter even numbers
  // Square them
  // Take first 5
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() async {
  await for (var value in numberStream()
      .where((n) => n % 2 == 0)
      .map((n) => n * n)
      .take(5)) {
    print(value);
  }
}

Stream<int> numberStream() async* {
  for (int i = 1; i <= 20; i++) {
    await Future.delayed(Duration(milliseconds: 100));
    yield i;
  }
}
```
</details>

</td>
<td width="50%" valign="top">

### 📝 Exercise 23: Custom Stream Controller
**Difficulty:** ⭐⭐⭐⭐

Create a custom event bus using StreamController.

```dart
void main() {
  var eventBus = EventBus();
  
  eventBus.on<String>().listen((event) {
    print('String event: $event');
  });
  
  eventBus.fire('Hello');
  eventBus.fire(42);
}
```

<details>
<summary>✅ Solution</summary>

```dart
import 'dart:async';

void main() {
  var eventBus = EventBus();
  
  eventBus.on<String>().listen((event) {
    print('String event: $event');
  });
  
  eventBus.on<int>().listen((event) {
    print('Int event: $event');
  });
  
  eventBus.fire('Hello');
  eventBus.fire(42);
  eventBus.fire('World');
}

class EventBus {
  final _controller = StreamController<dynamic>.broadcast();
  
  Stream<T> on<T>() {
    return _controller.stream.where((event) => event is T).cast<T>();
  }
  
  void fire(dynamic event) {
    _controller.add(event);
  }
  
  void dispose() {
    _controller.close();
  }
}
```
</details>

---

### 📝 Exercise 24: Async Queue
**Difficulty:** ⭐⭐⭐⭐

Implement an async queue that processes one item at a time.

<details>
<summary>💡 Hint</summary>

Use Completer and a list to queue tasks!
</details>

<details>
<summary>✅ Solution</summary>

```dart
import 'dart:async';

void main() async {
  var queue = AsyncQueue();
  
  queue.add(() => process('Task 1', 2));
  queue.add(() => process('Task 2', 1));
  queue.add(() => process('Task 3', 3));
}

Future<void> process(String name, int seconds) async {
  print('Starting $name');
  await Future.delayed(Duration(seconds: seconds));
  print('Completed $name');
}

class AsyncQueue {
  final List<Future Function()> _queue = [];
  bool _isProcessing = false;
  
  void add(Future Function() task) {
    _queue.add(task);
    _process();
  }
  
  Future<void> _process() async {
    if (_isProcessing) return;
    
    _isProcessing = true;
    while (_queue.isNotEmpty) {
      var task = _queue.removeAt(0);
      await task();
    }
    _isProcessing = false;
  }
}
```
</details>

</td>
</tr>
</table>

### 📝 Exercise 25-30: Async Challenges

<div align="center">

| # | 🎯 Challenge | 💪 Difficulty |
|:---:|:---|:---:|
| **25** | Implement retry logic with exponential backoff | ⭐⭐⭐⭐ |
| **26** | Create a rate limiter for API calls | ⭐⭐⭐⭐ |
| **27** | Build a timeout wrapper for Futures | ⭐⭐⭐ |
| **28** | Implement a cache with TTL (time to live) | ⭐⭐⭐⭐ |
| **29** | Create a stream debouncer | ⭐⭐⭐⭐ |
| **30** | Build a concurrent task pool with max workers | ⭐⭐⭐⭐⭐ |

</div>

---

## 🎯 Section 4: Design Patterns (31-40)

<div align="center">

### Professional Software Design

</div>

<table>
<tr>
<td width="50%" valign="top">

### 📝 Exercise 31: Repository Pattern
**Difficulty:** ⭐⭐⭐⭐

Create a repository for data access abstraction.

```dart
void main() async {
  UserRepository repo = UserRepository();
  
  await repo.create(User('1', 'John'));
  User? user = await repo.getById('1');
  print(user?.name);
}

class User {
  final String id;
  final String name;
  User(this.id, this.name);
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() async {
  UserRepository repo = UserRepository();
  
  await repo.create(User('1', 'John'));
  await repo.create(User('2', 'Alice'));
  
  User? user = await repo.getById('1');
  print('Found: ${user?.name}');
  
  List<User> all = await repo.getAll();
  print('Total users: ${all.length}');
  
  await repo.delete('1');
}

class User {
  final String id;
  final String name;
  User(this.id, this.name);
}

abstract class Repository<T> {
  Future<void> create(T item);
  Future<T?> getById(String id);
  Future<List<T>> getAll();
  Future<void> update(T item);
  Future<void> delete(String id);
}

class UserRepository implements Repository<User> {
  final Map<String, User> _storage = {};
  
  @override
  Future<void> create(User item) async {
    await Future.delayed(Duration(milliseconds: 100));
    _storage[item.id] = item;
    print('Created user: ${item.name}');
  }
  
  @override
  Future<User?> getById(String id) async {
    await Future.delayed(Duration(milliseconds: 50));
    return _storage[id];
  }
  
  @override
  Future<List<User>> getAll() async {
    await Future.delayed(Duration(milliseconds: 100));
    return _storage.values.toList();
  }
  
  @override
  Future<void> update(User item) async {
    await Future.delayed(Duration(milliseconds: 100));
    _storage[item.id] = item;
  }
  
  @override
  Future<void> delete(String id) async {
    await Future.delayed(Duration(milliseconds: 100));
    _storage.remove(id);
    print('Deleted user: $id');
  }
}
```
</details>

---

### 📝 Exercise 32: State Pattern
**Difficulty:** ⭐⭐⭐⭐

Implement state pattern for a vending machine.

```dart
void main() {
  var machine = VendingMachine();
  machine.insertMoney();
  machine.selectProduct();
  machine.dispense();
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  var machine = VendingMachine();
  
  machine.insertMoney();
  machine.selectProduct();
  machine.dispense();
  machine.dispense(); // Can't dispense again
}

abstract class VendingMachineState {
  void insertMoney(VendingMachine machine);
  void selectProduct(VendingMachine machine);
  void dispense(VendingMachine machine);
}

class IdleState implements VendingMachineState {
  @override
  void insertMoney(VendingMachine machine) {
    print('Money inserted');
    machine.setState(HasMoneyState());
  }
  
  @override
  void selectProduct(VendingMachine machine) {
    print('Please insert money first');
  }
  
  @override
  void dispense(VendingMachine machine) {
    print('Please insert money and select product');
  }
}

class HasMoneyState implements VendingMachineState {
  @override
  void insertMoney(VendingMachine machine) {
    print('Money already inserted');
  }
  
  @override
  void selectProduct(VendingMachine machine) {
    print('Product selected');
    machine.setState(DispensingState());
  }
  
  @override
  void dispense(VendingMachine machine) {
    print('Please select a product');
  }
}

class DispensingState implements VendingMachineState {
  @override
  void insertMoney(VendingMachine machine) {
    print('Please wait, dispensing product');
  }
  
  @override
  void selectProduct(VendingMachine machine) {
    print('Already dispensing');
  }
  
  @override
  void dispense(VendingMachine machine) {
    print('Dispensing product...');
    machine.setState(IdleState());
  }
}

class VendingMachine {
  VendingMachineState _state = IdleState();
  
  void setState(VendingMachineState state) {
    _state = state;
  }
  
  void insertMoney() => _state.insertMoney(this);
  void selectProduct() => _state.selectProduct(this);
  void dispense() => _state.dispense(this);
}
```
</details>

</td>
<td width="50%" valign="top">

### 📝 Exercise 33: Chain of Responsibility
**Difficulty:** ⭐⭐⭐⭐

Create a logging system with different levels.

```dart
void main() {
  var logger = InfoLogger()
    ..setNext(WarningLogger())
    ..setNext(ErrorLogger());
  
  logger.log('Info message', LogLevel.info);
  logger.log('Warning!', LogLevel.warning);
  logger.log('Error!', LogLevel.error);
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  var logger = InfoLogger()
    ..setNext(WarningLogger()
      ..setNext(ErrorLogger()));
  
  logger.log('Just info', LogLevel.info);
  logger.log('Be careful!', LogLevel.warning);
  logger.log('Critical error!', LogLevel.error);
}

enum LogLevel { info, warning, error }

abstract class Logger {
  Logger? _nextLogger;
  
  void setNext(Logger logger) {
    _nextLogger = logger;
  }
  
  void log(String message, LogLevel level) {
    if (canHandle(level)) {
      write(message);
    }
    
    if (_nextLogger != null) {
      _nextLogger!.log(message, level);
    }
  }
  
  bool canHandle(LogLevel level);
  void write(String message);
}

class InfoLogger extends Logger {
  @override
  bool canHandle(LogLevel level) => level == LogLevel.info;
  
  @override
  void write(String message) {
    print('[INFO] $message');
  }
}

class WarningLogger extends Logger {
  @override
  bool canHandle(LogLevel level) => level == LogLevel.warning;
  
  @override
  void write(String message) {
    print('[WARNING] ⚠️  $message');
  }
}

class ErrorLogger extends Logger {
  @override
  bool canHandle(LogLevel level) => level == LogLevel.error;
  
  @override
  void write(String message) {
    print('[ERROR] ❌ $message');
  }
}
```
</details>

---

### 📝 Exercise 34: Dependency Injection
**Difficulty:** ⭐⭐⭐⭐

Create a simple DI container.

<details>
<summary>💡 Hint</summary>

Use a Map to register and resolve dependencies!
</details>

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  var container = DIContainer();
  
  // Register dependencies
  container.register<Database>(() => Database());
  container.register<UserService>(() => 
    UserService(container.resolve<Database>()));
  
  // Resolve and use
  var service = container.resolve<UserService>();
  service.getUser('123');
}

class Database {
  void query(String sql) => print('Executing: $sql');
}

class UserService {
  final Database db;
  UserService(this.db);
  
  void getUser(String id) {
    db.query('SELECT * FROM users WHERE id = $id');
  }
}

class DIContainer {
  final Map<Type, dynamic Function()> _factories = {};
  final Map<Type, dynamic> _singletons = {};
  
  void register<T>(T Function() factory, {bool singleton = false}) {
    _factories[T] = factory;
    if (singleton) {
      _singletons[T] = factory();
    }
  }
  
  T resolve<T>() {
    if (_singletons.containsKey(T)) {
      return _singletons[T] as T;
    }
    
    var factory = _factories[T];
    if (factory == null) {
      throw Exception('Type $T not registered');
    }
    
    return factory() as T;
  }
}
```
</details>

</td>
</tr>
</table>

### 📝 Exercise 35-40: Pattern Challenges

<div align="center">

| # | 🎯 Challenge | 💪 Difficulty |
|:---:|:---|:---:|
| **35** | Implement Mediator pattern for component communication | ⭐⭐⭐⭐ |
| **36** | Create Template Method pattern for algorithms | ⭐⭐⭐ |
| **37** | Build Proxy pattern for lazy loading | ⭐⭐⭐⭐ |
| **38** | Implement Facade pattern for complex subsystem | ⭐⭐⭐ |
| **39** | Create Memento pattern for undo/redo | ⭐⭐⭐⭐⭐ |
| **40** | Build Visitor pattern for object structure operations | ⭐⭐⭐⭐⭐ |

</div>

---

## 🧮 Section 5: Algorithms & Data Structures (41-50)

<div align="center">

### Computer Science Fundamentals

</div>

<table>
<tr>
<td width="50%" valign="top">

### 📝 Exercise 41: Binary Search Tree
**Difficulty:** ⭐⭐⭐⭐

Implement a BST with insert, search, and traverse.

```dart
void main() {
  var bst = BST();
  [5, 3, 7, 1, 9, 4, 6].forEach(bst.insert);
  
  print(bst.search(4)); // true
  print(bst.search(10)); // false
  
  bst.inorderTraversal(); // 1 3 4 5 6 7 9
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  var bst = BST();
  [5, 3, 7, 1, 9, 4, 6].forEach(bst.insert);
  
  print('Search 4: ${bst.search(4)}');
  print('Search 10: ${bst.search(10)}');
  
  print('Inorder: ');
  bst.inorderTraversal();
}

class Node {
  int value;
  Node? left, right;
  Node(this.value);
}

class BST {
  Node? root;
  
  void insert(int value) {
    root = _insertRec(root, value);
  }
  
  Node _insertRec(Node? node, int value) {
    if (node == null) {
      return Node(value);
    }
    
    if (value < node.value) {
      node.left = _insertRec(node.left, value);
    } else if (value > node.value) {
      node.right = _insertRec(node.right, value);
    }
    
    return node;
  }
  
  bool search(int value) {
    return _searchRec(root, value);
  }
  
  bool _searchRec(Node? node, int value) {
    if (node == null) return false;
    if (node.value == value) return true;
    
    if (value < node.value) {
      return _searchRec(node.left, value);
    } else {
      return _searchRec(node.right, value);
    }
  }
  
  void inorderTraversal() {
    _inorderRec(root);
    print('');
  }
  
  void _inorderRec(Node? node) {
    if (node != null) {
      _inorderRec(node.left);
      print('${node.value} ');
      _inorderRec(node.right);
    }
  }
}
```
</details>

---

### 📝 Exercise 42: Graph BFS & DFS
**Difficulty:** ⭐⭐⭐⭐⭐

Implement breadth-first and depth-first search.

<details>
<summary>💡 Hint</summary>

Use Queue for BFS and Stack (recursion) for DFS!
</details>

</td>
<td width="50%" valign="top">

### 📝 Exercise 43: Dynamic Programming
**Difficulty:** ⭐⭐⭐⭐⭐

Solve the coin change problem using DP.

```dart
void main() {
  List<int> coins = [1, 5, 10, 25];
  int amount = 30;
  
  print(minCoins(coins, amount)); // 2 (25 + 5)
}

int minCoins(List<int> coins, int amount) {
  // Your implementation using DP
}
```

<details>
<summary>✅ Solution</summary>

```dart
void main() {
  List<int> coins = [1, 5, 10, 25];
  int amount = 30;
  
  print('Min coins needed: ${minCoins(coins, amount)}');
}

int minCoins(List<int> coins, int amount) {
  List<int> dp = List.filled(amount + 1, amount + 1);
  dp[0] = 0;
  
  for (int i = 1; i <= amount; i++) {
    for (int coin in coins) {
      if (coin <= i) {
        dp[i] = dp[i] < dp[i - coin] + 1 
          ? dp[i] 
          : dp[i - coin] + 1;
      }
    }
  }
  
  return dp[amount] > amount ? -1 : dp[amount];
}
```
</details>

---

### 📝 Exercise 44: LRU Cache
**Difficulty:** ⭐⭐⭐⭐⭐

Implement a Least Recently Used cache.

<details>
<summary>💡 Hint</summary>

Use a combination of Map and LinkedList!
</details>

</td>
</tr>
</table>

### 📝 Exercise 45-50: Algorithm Challenges

<div align="center">

| # | 🎯 Challenge | 💪 Difficulty |
|:---:|:---|:---:|
| **45** | Implement Dijkstra's shortest path algorithm | ⭐⭐⭐⭐⭐ |
| **46** | Create a Trie for efficient string searching | ⭐⭐⭐⭐ |
| **47** | Solve the N-Queens problem using backtracking | ⭐⭐⭐⭐⭐ |
| **48** | Implement merge sort and quick sort | ⭐⭐⭐⭐ |
| **49** | Build a priority queue (min heap) | ⭐⭐⭐⭐ |
| **50** | Solve the knapsack problem with DP | ⭐⭐⭐⭐⭐ |

</div>

---

## 🔥 Challenge Projects

<div align="center">

### Put Everything Together! 🚀

</div>

### 🏆 Project 1: Task Scheduler
**Level:** Advanced  
**Topics:** Async, Design Patterns, Data Structures

Build a task scheduler that:
- Accepts tasks with priorities and dependencies
- Executes tasks asynchronously with concurrency limits
- Implements retry logic with exponential backoff
- Tracks task progress and results
- Supports cancellation

**Key Patterns:** Observer, Command, Strategy

---

### 🏆 Project 2: In-Memory Database
**Level:** Advanced  
**Topics:** Data Structures, Algorithms, OOP

Create a simple in-memory database with:
- CRUD operations (Create, Read, Update, Delete)
- Indexing for fast lookups
- Query filtering and sorting
- Transaction support (begin, commit, rollback)
- Concurrent access handling

**Key Structures:** BST, Hash Map, Transaction Manager

---

### 🏆 Project 3: Rate-Limited API Client
**Level:** Advanced  
**Topics:** Async, Design Patterns, Concurrency

Build an API client that:
- Enforces rate limits (requests per second/minute)
- Implements request queuing
- Supports retry with backoff
- Caches responses with TTL
- Handles circuit breaking for failing services

**Key Patterns:** Singleton, Proxy, State

---

### 🏆 Project 4: Event-Driven System
**Level:** Advanced  
**Topics:** Async, Streams, Design Patterns

Develop an event system with:
- Event bus for pub/sub
- Event sourcing (store all events)
- Event replay capabilities
- Async event handlers
- Dead letter queue for failed events

**Key Patterns:** Observer, Mediator, Chain of Responsibility

---

### 🏆 Project 5: Functional Data Pipeline
**Level:** Advanced  
**Topics:** Functional Programming, Streams, Async

Create a data processing pipeline that:
- Reads data from multiple sources
- Applies transformations (map, filter, reduce)
- Handles errors gracefully
- Supports parallel processing
- Writes to multiple destinations

**Key Concepts:** Lazy evaluation, Stream transformations, Composition

---

## 📚 Additional Resources

<div align="center">

### 🎓 Continue Your Journey!

[![Effective Dart](https://img.shields.io/badge/Effective-Dart-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/guides/language/effective-dart)
[![Design Patterns](https://img.shields.io/badge/Design-Patterns-orange?style=for-the-badge)](https://refactoring.guru/design-patterns)
[![Algorithms](https://img.shields.io/badge/Algorithms-LeetCode-FFA116?style=for-the-badge)](https://leetcode.com/)
[![Architecture](https://img.shields.io/badge/Clean-Architecture-success?style=for-the-badge)](https://blog.cleancoder.com/)

</div>

#### 🌟 Advanced Learning
- 📖 [Dart Language Specification](https://dart.dev/guides/language/spec) - Deep dive
- 🏗️ [Design Patterns in Dart](https://refactoring.guru/design-patterns) - Comprehensive guide
- 🧮 [Algorithms & Data Structures](https://visualgo.net/) - Visual learning
- ⚡ [Async Programming Guide](https://dart.dev/codelabs/async-await) - Master async/await
- 🎯 [Functional Programming in Dart](https://dart.dev/guides/language/language-tour#functions) - FP concepts

---

## 💡 Mastery Tips

```
┌──────────────────────────────────────────────┐
│  ✅ Focus on understanding, not memorization │
│  ✅ Implement patterns from scratch           │
│  ✅ Refactor constantly                       │
│  ✅ Profile and optimize                      │
│  ✅ Write tests for everything                │
│  ✅ Read others' code                         │
│  ✅ Contribute to open source                 │
└──────────────────────────────────────────────┘
```

### 🎯 Progress Tracking

<div align="center">

| 📊 Skill Area | 🎯 Target | ✅ Complete |
|:---|:---:|:---:|
| **Functional Programming** | 10 exercises | ☐ |
| **Advanced OOP** | 10 exercises | ☐ |
| **Async & Concurrency** | 10 exercises | ☐ |
| **Design Patterns** | 10 exercises | ☐ |
| **Algorithms & DS** | 10 exercises | ☐ |
| **Challenge Projects** | 5 projects | ☐ |

</div>

---

<div align="center">

### 💙 *"Any fool can write code that a computer can understand. Good programmers write code that humans can understand."* – Martin Fowler

**Keep Practicing, Keep Improving! 🚀✨**

---

Made with 💙 by the Dart community

[⬆ Back to top](#-dart-intermediate-exercises-)

</div>
