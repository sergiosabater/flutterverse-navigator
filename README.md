<div align="center">

# 🧪 Flutter Exercises – Beginner Level 🚀

### *Your practical path to mastering Flutter from scratch*

[![Flutter](https://img.shields.io/badge/Flutter-Beginner-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://docs.flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-Basics-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
[![Level](https://img.shields.io/badge/Level-Beginner-brightgreen?style=for-the-badge)]()

**10 hands-on exercises to build your Flutter foundation**  
`Widgets` • `Layouts` • `State` • `Navigation`

---

</div>

## 🎯 About This Guide

This section contains a series of **practical Flutter exercises** designed for people who are starting from scratch. The goal is to solidify the basic concepts of **Dart**, **widgets**, **layouts**, and **state** through real, working code.

```dart
void main() {
  runApp(
    MaterialApp(
      home: YourFirstApp(), // 👈 Your journey starts here!
    ),
  );
}
```

---

## 📌 Prerequisites

<div align="center">

| ✅ Requirement | 📝 Description |
|:---:|:---|
| **Flutter SDK** | Properly installed on your system |
| **Code Editor** | VS Code or Android Studio recommended |
| **Device** | Emulator or physical device running |
| **Programming Basics** | Variables, functions, classes |

</div>

---

## 🏋️ Exercise Breakdown

```
┌─────────────────────────────────────────┐
│  🟢 Basic Widgets (Ex 1-4)              │
│  🟡 Interactivity & State (Ex 5-7)      │
│  🔵 Advanced Concepts (Ex 8-10)         │
└─────────────────────────────────────────┘
```

---

## 🟢 Basic Widgets

<table>
<tr>
<td width="50%" valign="top">

### **Exercise 1: Hello World in Flutter**

#### 🎯 Objective
Create a Flutter application that displays centered text on the screen.

#### 📋 Instructions
- Create a new Flutter project
- Use a `MaterialApp`
- Display the text **"Hello Flutter 👋"** centered on the screen

#### 💡 Hints
```dart
// Widgets to use:
Scaffold
Center
Text
```

</td>
<td width="50%" valign="top">

### **Exercise 2: Styled Text**

#### 🎯 Objective
Learn to apply styles to a `Text`.

#### 📋 Instructions
- Display a text with:
  - Size 24
  - Blue color
  - Bold
- Center the text on the screen

#### 💡 Hints
```dart
// Use TextStyle:
TextStyle(
  fontSize: 24,
  color: Colors.blue,
  fontWeight: FontWeight.bold,
)
```

</td>
</tr>
</table>

---

<table>
<tr>
<td width="50%" valign="top">

### **Exercise 3: Column of Texts**

#### 🎯 Objective
Work with vertical layouts.

#### 📋 Instructions
- Display three texts one below the other:
  - "Flutter"
  - "is"
  - "awesome 🚀"
- Center the column vertically and horizontally

#### 💡 Hints
```dart
// Use Column:
Column(
  mainAxisAlignment: MainAxisAlignment.center,
  crossAxisAlignment: CrossAxisAlignment.center,
  children: [...]
)
```

</td>
<td width="50%" valign="top">

### **Exercise 4: Image from the Internet**

#### 🎯 Objective
Display images in Flutter.

#### 📋 Instructions
- Display an image from a URL
- It must have a maximum width of 200 px

#### 💡 Hints
```dart
// Use Image.network:
Image.network(
  'https://example.com/image.png',
  width: 200,
)
```

</td>
</tr>
</table>

---

## 🟡 Interactivity & State

<table>
<tr>
<td width="50%" valign="top">

### **Exercise 5: Button and Action**

#### 🎯 Objective
Detect user interaction.

#### 📋 Instructions
- Add a button
- When pressed, show a `SnackBar` with the text:
  > "Button pressed"

#### 💡 Hints
```dart
// Use ElevatedButton:
ElevatedButton(
  onPressed: () {
    ScaffoldMessenger.of(context)
      .showSnackBar(...);
  },
  child: Text('Press Me'),
)
```

</td>
<td width="50%" valign="top">

### **Exercise 6: Simple Counter**

#### 🎯 Objective
Introduction to state in Flutter.

#### 📋 Instructions
- Create a counter that:
  - Starts at 0
  - Has a button to increment
  - Displays the value on screen

#### 💡 Hints
```dart
// Use StatefulWidget:
class Counter extends StatefulWidget {
  // Use setState() to update UI
}
```

</td>
</tr>
</table>

---

<div align="center">

### **Exercise 7: List of Elements**

#### 🎯 Objective
Work with dynamic lists.

#### 📋 Instructions
- Display a list with at least 5 text elements
- Each element must be a `ListTile`

#### 💡 Hints
```dart
// Use ListView:
ListView(
  children: [
    ListTile(title: Text('Item 1')),
    ListTile(title: Text('Item 2')),
    // ...
  ],
)

// Or use ListView.builder for dynamic lists
```

</div>

---

## 🔵 Advanced Concepts

<table>
<tr>
<td width="50%" valign="top">

### **Exercise 8: Custom Card**

#### 🎯 Objective
Learn to use `Card`.

#### 📋 Instructions
- Create a `Card` with:
  - Internal padding
  - A title
  - A description
- Center the card on the screen

#### 💡 Hints
```dart
// Use Card widget:
Card(
  child: Padding(
    padding: EdgeInsets.all(16),
    child: Column(...),
  ),
)
```

</td>
<td width="50%" valign="top">

### **Exercise 9: Navigation Between Screens**

#### 🎯 Objective
Navigate between two screens.

#### 📋 Instructions
- Screen A with a button
- When pressed, navigate to Screen B
- On Screen B display a text

#### 💡 Hints
```dart
// Use Navigator.push:
Navigator.push(
  context,
  MaterialPageRoute(
    builder: (context) => ScreenB(),
  ),
);
```

</td>
</tr>
</table>

---

<div align="center">

## 🏆 Exercise 10: Final Mini Challenge

### 🎯 Objective
Apply everything learned.

### 📋 Instructions
Create an app that has:

| Component | Description |
|:---:|:---|
| **AppBar** | With a title |
| **Counter** | Starting at 0 |
| **Button** | To increment the counter |
| **Dynamic List** | That grows with each button press |

### 💡 Hints
```dart
// Combine concepts:
// - StatefulWidget
// - List management
// - setState()
// - ListView.builder
```

</div>

---

## ✅ Recommendations

<div align="center">

### Best practices to maximize your learning

| 💎 Recommendation | 📝 Why it matters |
|:---|:---|
| **Don't copy and paste** | Type the code yourself to build muscle memory |
| **Experiment with values** | Change colors, sizes, and see what happens |
| **Break things intentionally** | Learn by fixing errors |
| **Read error messages** | They're your best teacher |
| **Consult documentation** | [docs.flutter.dev](https://docs.flutter.dev/) is your friend |

</div>

---

## 🚀 Next Steps

<div align="center">

```
┌─────────────────────────────────────────┐
│  ✨ After completing these exercises:   │
│                                          │
│  📦 Refactor your code                   │
│  🧩 Practice widget separation           │
│  🔄 Master StatelessWidget vs            │
│     StatefulWidget                       │
│  🎨 Explore advanced layouts             │
│  📚 Study state management patterns      │
└─────────────────────────────────────────┘
```

### 📚 Continue Your Journey

[![Flutter Docs](https://img.shields.io/badge/Flutter-Documentation-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://docs.flutter.dev/)
[![Dart Tour](https://img.shields.io/badge/Dart-Language%20Tour-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/guides/language/language-tour)
[![Cookbook](https://img.shields.io/badge/Flutter-Cookbook-20232A?style=for-the-badge&logo=flutter&logoColor=61DAFB)](https://docs.flutter.dev/cookbook)

</div>

---

## 📊 Progress Tracker

<div align="center">

Track your journey through the exercises:

![Exercise 1](https://img.shields.io/badge/Ex%201-Hello%20World-brightgreen?style=flat-square)
![Exercise 2](https://img.shields.io/badge/Ex%202-Styled%20Text-brightgreen?style=flat-square)
![Exercise 3](https://img.shields.io/badge/Ex%203-Column-brightgreen?style=flat-square)
![Exercise 4](https://img.shields.io/badge/Ex%204-Images-brightgreen?style=flat-square)
![Exercise 5](https://img.shields.io/badge/Ex%205-Buttons-yellow?style=flat-square)
![Exercise 6](https://img.shields.io/badge/Ex%206-Counter-yellow?style=flat-square)
![Exercise 7](https://img.shields.io/badge/Ex%207-Lists-yellow?style=flat-square)
![Exercise 8](https://img.shields.io/badge/Ex%208-Cards-blue?style=flat-square)
![Exercise 9](https://img.shields.io/badge/Ex%209-Navigation-blue?style=flat-square)
![Exercise 10](https://img.shields.io/badge/Ex%2010-Challenge-blue?style=flat-square)

</div>

---

<div align="center">

### 💙 *"The expert in anything was once a beginner."*

**Happy learning and enjoy Flutter! 🦋✨**

---

Made with 💙 for Flutter beginners

[⬆ Back to top](#-flutter-exercises--beginner-level-)

</div>
