<div align="center">

# 🚀 Flutter Exercises – Intermediate Level 💪

### *Level up your Flutter skills with real-world projects*

[![Flutter](https://img.shields.io/badge/Flutter-Intermediate-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://docs.flutter.dev/)
[![Dart](https://img.shields.io/badge/Dart-Advanced-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dart.dev/)
[![Level](https://img.shields.io/badge/Level-Intermediate-orange?style=for-the-badge)]()

**11 real-world projects to master Flutter development**  
`State Management` • `APIs` • `Animations` • `Local Storage` • `Complex Navigation`

---

</div>

## 🎯 About This Guide

This collection features **intermediate Flutter exercises** designed to bridge the gap between basics and production-ready applications. Each project incorporates multiple concepts and mirrors real-world app development scenarios.

```dart
void main() {
  runApp(
    MaterialApp(
      home: YourProductionApp(), // 👈 Build something real!
    ),
  );
}
```

---

## 🏗️ Exercise Categories

```
┌─────────────────────────────────────────┐
│  🎨 State Management (Ex 1, 6)          │
│  🌐 API Integration (Ex 2, 8)           │
│  ✨ Animations (Ex 3, 9)                │
│  📝 Forms & Validation (Ex 4)           │
│  💾 Local Storage (Ex 5, 6)             │
│  🎵 Media & Files (Ex 7)                │
│  🧭 Complex Navigation (Ex 10)          │
│  📊 Data Visualization (Bonus)          │
└─────────────────────────────────────────┘
```

---

## 📱 Projects Overview

<table>
<tr>
<td width="50%" valign="top">

### **Exercise 1: Task Manager with State**

#### 🎯 Objective
Create a task list application with state management using Provider or Riverpod.

#### 📋 Requirements
- Add, edit, and delete tasks
- Mark tasks as completed
- Filter tasks by status (all, active, completed)
- Persist data using SharedPreferences
- Implement pending tasks counter

#### 💡 Key Concepts
```dart
// State management patterns:
- Provider / Riverpod
- SharedPreferences
- StatefulWidget
- ChangeNotifier
```

</td>
<td width="50%" valign="top">

### **Exercise 2: Weather App with API**

#### 🎯 Objective
Develop an app that queries a weather API and displays current conditions.

#### 📋 Requirements
- Integrate API (OpenWeatherMap or similar)
- Display temperature, conditions, and forecast
- Implement city search
- Add error handling and loading states
- Data caching with expiration time
- Responsive UI with different layouts

#### 💡 Key Concepts
```dart
// API integration:
- HTTP requests (http/dio)
- Future & async/await
- JSON parsing
- Error handling
```

</td>
</tr>
</table>

---

<table>
<tr>
<td width="50%" valign="top">

### **Exercise 3: Image Carousel with Animations**

#### 🎯 Objective
Create an image carousel with custom animated transitions.

#### 📋 Requirements
- Horizontal swipe with PageView
- Custom entrance/exit animations
- Page indicators
- Zoom and pan on images
- Lazy loading of images
- Implement Hero animations between screens

#### 💡 Key Concepts
```dart
// Animation mastery:
- AnimationController
- Tween
- PageController
- GestureDetector
- Hero transitions
```

</td>
<td width="50%" valign="top">

### **Exercise 4: Complex Registration Form**

#### 🎯 Objective
Develop a multi-step form with advanced validation.

#### 📋 Requirements
- 3-4 form steps
- Real-time validation
- Fields: email, password, phone, birthdate
- Password confirmation
- Country selection dropdown
- Display form progress
- Save data temporarily when changing steps

#### 💡 Key Concepts
```dart
// Form handling:
- Form & TextFormField
- Validation patterns
- RegExp
- Stepper widget
- State preservation
```

</td>
</tr>
</table>

---

<table>
<tr>
<td width="50%" valign="top">

### **Exercise 5: Chat with Local Database**

#### 🎯 Objective
Create a chat application with local storage using SQLite.

#### 📋 Requirements
- Conversation list
- Individual message view
- Send and receive messages (simulated)
- Timestamps and read status
- Message search
- Delete conversations
- Implement pagination in message list

#### 💡 Key Concepts
```dart
// Database operations:
- sqflite
- FutureBuilder
- ListView.builder
- CRUD operations
- Pagination
```

</td>
<td width="50%" valign="top">

### **Exercise 6: Notes App with Search & Categories**

#### 🎯 Objective
Develop a notes application with advanced features.

#### 📋 Requirements
- Create, edit, delete notes
- Categories with custom colors
- Real-time search
- Sort by date, title, or category
- Grid and list view
- Share notes as text
- Light/dark theme

#### 💡 Key Concepts
```dart
// Advanced UI:
- SearchDelegate
- GridView
- Theme management
- Share plugin
- View switching
```

</td>
</tr>
</table>

---

<table>
<tr>
<td width="50%" valign="top">

### **Exercise 7: Music Player**

#### 🎯 Objective
Create a music player with complete controls.

#### 📋 Requirements
- Song list (from assets or local files)
- Play, pause, next, previous
- Interactive progress bar
- Shuffle and repeat
- Song artwork
- Lock screen controls
- Playlist

#### 💡 Key Concepts
```dart
// Media handling:
- audioplayers package
- StreamBuilder
- ValueNotifier
- Duration formatting
- Background audio
```

</td>
<td width="50%" valign="top">

### **Exercise 8: Photo Gallery with Infinite Scroll**

#### 🎯 Objective
Implement a gallery that loads images dynamically from an API.

#### 📋 Requirements
- Integrate image API (Unsplash, Pixabay)
- Infinite scroll with end-of-list detection
- Responsive grid layout
- Detail screen with zoom
- Download images to gallery
- Locally saved favorites
- Pull-to-refresh

#### 💡 Key Concepts
```dart
// Infinite loading:
- ScrollController
- Pagination
- NetworkImage
- Image caching
- Pull to refresh
```

</td>
</tr>
</table>

---

<table>
<tr>
<td width="50%" valign="top">

### **Exercise 9: Tip Calculator with Bill Splitter**

#### 🎯 Objective
Create a calculator with animations and polished UI.

#### 📋 Requirements
- Calculate tip by percentage
- Split bill among people
- Round up/down
- Calculation history
- Animations when changing values
- Currency selector
- Portrait and landscape modes

#### 💡 Key Concepts
```dart
// UI polish:
- NumberFormat
- OrientationBuilder
- AnimatedContainer
- Custom painters
- Responsive layouts
```

</td>
<td width="50%" valign="top">

### **Exercise 10: Recipe App with Complex Navigation**

#### 🎯 Objective
Develop a recipe app with nested navigation and tabs.

#### 📋 Requirements
- Bottom navigation with 3 tabs
- Recipe list by category
- Recipe detail with ingredients and steps
- Navigation to related recipes
- Favorites with persistence
- Integrated cooking timer
- Search and filters

#### 💡 Key Concepts
```dart
// Navigation patterns:
- Named routes
- BottomNavigationBar
- TabBarView
- Nested navigation
- Timer widget
```

</td>
</tr>
</table>

---

<div align="center">

## 🎁 Bonus Exercise: Dashboard with Charts

### 🎯 Objective
Create a dashboard with different types of interactive charts.

### 📋 Requirements

| Feature | Description |
|:---:|:---|
| **Line Chart** | For trend visualization |
| **Bar Chart** | For comparisons |
| **Pie Chart** | For percentages |
| **Date Filters** | Range selection |
| **Animations** | On data load |
| **Export** | Save charts as images |

### 💡 Key Concepts
```dart
// Data visualization:
- fl_chart package
- CustomPaint
- DatePicker
- Screenshot capture
- Chart animations
```

</div>

---

## 💎 Best Practices for These Exercises

<div align="center">

| 🏆 Practice | 📝 Implementation | 🎯 Why It Matters |
|:---|:---|:---|
| **Clean Architecture** | Separate business logic from UI | Maintainability & testability |
| **Error Handling** | Always implement try-catch and error states | Better UX & debugging |
| **Loading States** | Show indicators while loading data | User feedback |
| **Responsive Design** | Test on different screen sizes | Cross-device compatibility |
| **Accessibility** | Add Semantics and descriptive texts | Inclusive design |
| **Testing** | Write unit tests for business logic | Code reliability |
| **Performance** | Use const constructors, avoid unnecessary rebuilds | Smooth 60 FPS |

</div>

---

## 🛠️ Recommended Packages

```
┌─────────────────────────────────────────┐
│  📦 Essential Packages for These        │
│     Exercises:                           │
│                                          │
│  • provider / riverpod (state)          │
│  • http / dio (networking)              │
│  • shared_preferences (storage)         │
│  • sqflite (database)                   │
│  • cached_network_image (images)        │
│  • fl_chart (charts)                    │
│  • audioplayers (audio)                 │
│  • share_plus (sharing)                 │
└─────────────────────────────────────────┘
```

---

## 📊 Difficulty Breakdown

<div align="center">

### Each exercise focuses on specific skills

![Ex 1](https://img.shields.io/badge/Ex%201-State%20Management-orange?style=flat-square)
![Ex 2](https://img.shields.io/badge/Ex%202-API%20Integration-orange?style=flat-square)
![Ex 3](https://img.shields.io/badge/Ex%203-Animations-red?style=flat-square)
![Ex 4](https://img.shields.io/badge/Ex%204-Forms-orange?style=flat-square)
![Ex 5](https://img.shields.io/badge/Ex%205-Database-red?style=flat-square)

![Ex 6](https://img.shields.io/badge/Ex%206-Search%20%26%20Filters-orange?style=flat-square)
![Ex 7](https://img.shields.io/badge/Ex%207-Media%20Player-red?style=flat-square)
![Ex 8](https://img.shields.io/badge/Ex%208-Infinite%20Scroll-orange?style=flat-square)
![Ex 9](https://img.shields.io/badge/Ex%209-UI%20Polish-orange?style=flat-square)
![Ex 10](https://img.shields.io/badge/Ex%2010-Navigation-red?style=flat-square)
![Bonus](https://img.shields.io/badge/Bonus-Charts-purple?style=flat-square)

</div>

---

## 🚀 Getting Started

```bash
# Install required packages
flutter pub add provider http shared_preferences

# For specific exercises, install additional packages:
flutter pub add sqflite path  # Exercise 5
flutter pub add audioplayers   # Exercise 7
flutter pub add fl_chart       # Bonus exercise

# Run your project
flutter run
```

---

## 📚 Additional Resources

<div align="center">

### Level up your Flutter knowledge

[![Documentation](https://img.shields.io/badge/Flutter-Documentation-02569B?style=for-the-badge&logo=flutter&logoColor=white)](https://docs.flutter.dev/)
[![Pub.dev](https://img.shields.io/badge/Pub.dev-Packages-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://pub.dev/)
[![Cookbook](https://img.shields.io/badge/Flutter-Cookbook-20232A?style=for-the-badge&logo=flutter&logoColor=61DAFB)](https://docs.flutter.dev/cookbook)
[![DartPad](https://img.shields.io/badge/DartPad-Practice-0175C2?style=for-the-badge&logo=dart&logoColor=white)](https://dartpad.dev/)

</div>

#### 🎓 Learning Path
- 📖 [State Management Guide](https://docs.flutter.dev/development/data-and-backend/state-mgmt/intro)
- 🌐 [Networking & HTTP](https://docs.flutter.dev/development/data-and-backend/networking)
- ✨ [Animation Tutorial](https://docs.flutter.dev/development/ui/animations)
- 💾 [Persistence Documentation](https://docs.flutter.dev/cookbook/persistence)
- 🧭 [Navigation & Routing](https://docs.flutter.dev/development/ui/navigation)

---

## 🎯 Project Completion Checklist

<div align="center">

For each exercise, ensure you've implemented:

| ✅ Criterion | Description |
|:---:|:---|
| **Functionality** | All requirements working correctly |
| **Error Handling** | Graceful error states and messages |
| **Loading States** | User feedback during operations |
| **Code Quality** | Clean, organized, and commented code |
| **UI/UX** | Intuitive and visually appealing interface |
| **Performance** | Smooth animations, no jank |
| **Testing** | Basic unit tests for business logic |

</div>

---

## 💡 Pro Tips

<table>
<tr>
<td width="50%" valign="top">

### 🎨 **UI/UX Excellence**
- Use Material 3 design guidelines
- Implement proper spacing and alignment
- Add subtle animations for delight
- Consider accessibility from the start
- Test on multiple screen sizes

</td>
<td width="50%" valign="top">

### ⚡ **Performance Optimization**
- Use `const` constructors everywhere possible
- Implement `ListView.builder` for long lists
- Cache network images
- Avoid unnecessary `setState()` calls
- Profile with DevTools

</td>
</tr>
</table>

---

<div align="center">

### 💙 *"Code is like humor. When you have to explain it, it's bad."*

**Keep building amazing Flutter apps! 🚀✨**

---

Made with 💙 for Flutter developers

[⬆ Back to top](#-flutter-exercises--intermediate-level-)

</div>
