# CaptapApp

A scalable, cross-platform **Pharmacy Management System** built with **Flutter**
(Mobile • Tablet • Desktop)

---

## 📌 Project Overview

CaptapApp is a multi-platform pharmacy management system designed and implemented using Flutter, intended to serve real business workflows across mobile, tablet, and desktop devices.

This repository showcases the **architecture, design decisions, and code structure** of the project. The full production source code is not included due to confidentiality and code ownership constraints.

---

## 🚀 Key Features

* Modular architecture following **Clean Architecture** principles
* Organized state management using **BLoC**
* Local database integration with **sqflite**
* Responsive UI adapted for:

  * 📱 Mobile
  * 📊 Tablet
  * 🖥️ Desktop
* Integration with real device features:

  * QR code scanning
  * Barcode scanning
  * Camera access & permissions
  * Location and address handling
* Multi-language support (Arabic, English, Turkish)

---

## 🧠 Architecture & Design

CaptapApp was architected with **scalability and maintainability** in mind from the very beginning.

### 🔹 Clean Architecture

The project is structured into three main layers:

* **Presentation Layer**: UI + BLoC
* **Domain Layer**: Business logic & use cases
* **Data Layer**: Local and remote data sources

This separation allows:

* Easy feature expansion (Inventory, Suppliers, Reports, etc.)
* Clear responsibilities per layer
* Minimal impact when introducing new modules

---

## 📐 State Management

State is managed using **BLoC**, providing:

* Clear and predictable state transitions
* Centralized loading and error handling
* Clean separation between UI and business logic

Use cases are injected into BLoCs instead of being instantiated inside classes, ensuring better testability and maintainability.

---

## 💾 Local Storage

Local persistence is implemented using **sqflite**, supporting:

* Multiple relational tables
* Offline access
* Caching strategies for improved performance

---

## 🌐 Networking

Networking is implemented using **Dio**, featuring:

* Centralized API configuration
* Request and response validation
* Interceptors for:

  * Logging
  * Error handling
  * Request status monitoring

Abstract classes are used to reuse RESTful API methods and enforce consistent API contracts across the data layer.

---

## 📱 Responsive UI Strategy

The UI includes more than **380 screens**, all converted from Figma designs into a responsive Flutter interface.

### ❌ Why ScreenUtil Was Not Enough

Although ScreenUtil was initially used, it introduced limitations when:

* System font size increased (accessibility scenarios)
* Rendering layouts on tablets and desktops
* Maintaining predictable scaling across platforms

### ✅ Custom Config & Size Management

Instead of ScreenUtil, a **custom Config / SizeConfig approach** was implemented:

* Clear breakpoints for Mobile / Tablet / Desktop
* Centralized control for spacing, padding, and typography
* Respect for system font scaling
* Predictable and accessible layouts

Separate layout logic/classes are used for each device type, ensuring clarity and long-term maintainability.

---

## 🌍 Localization & Accessibility

### 🌐 Multi-Language Support

CaptapApp supports three languages:

* Arabic (RTL support)
* English
* Turkish

Localization is handled using a centralized **AppLocalization** system, allowing:

* Clean language switching
* Easy addition of new languages
* Separation of UI and translation resources

---

## 🎨 Theme & Color Management

All application colors are centralized using a **ColorManager** implemented as an **abstract class with static properties**:

* No hardcoded colors in UI widgets
* Consistent theming across the app
* Easy brand or theme updates

---

## 🔌 Dependency Injection

Dependency Injection is implemented using a **Service Locator** pattern:

* Organized object creation
* Lazy initialization when needed
* Clean dependency management across layers

---

## 🧠 Planning Before Coding

Before development started:

* Functional and non-functional requirements were defined
* Scalability paths and future modules were planned
* Core technical decisions (state management, storage, networking) were finalized

This planning resulted in a predictable and maintainable codebase suitable for large-scale business systems.

---

## 🎯 Client-Focused Development

Throughout the implementation:

* Real pharmacy workflows guided feature design
* UI/UX decisions matched real usage scenarios
* Device permissions were handled contextually across platforms

---

## 📸 Screenshots & Architecture Showcase

To respect code ownership, selected screenshots are included to demonstrate architectural decisions:

* **captap_mockup.png**: Cross-platform UI mockup
* **Screenshot (1494).png**: Centralized generateRoute navigation
* **Screenshot (1493).png**: BLoC usage with injected use cases
* **equtable.PNG**: Object comparison using Equatable
* **Screenshot (1492).png**: Dio networking with interceptors
* **Screenshot (1491).png**: Abstract classes for RESTful APIs
* **Screenshot (1490).png**: Dependency Injection as a Service Locator
* **size_config.PNG**: Custom screen size & breakpoint management
* **responsive.PNG**: Separate layouts for mobile, tablet, and desktop
* **abstract_static_color_manager.PNG**: Centralized color management
* **app_localization.PNG**: Multi-language implementation

---

## 🛠️ Built With

* Flutter
* Dart
* BLoC
* Clean Architecture
* sqflite
* Dio
* Dependency Injection
* Localization & Accessibility

---

## ▶️ Run the App

```bash
flutter run
```

---

## 📄 Notes

This repository is intended for **portfolio and architectural demonstration purposes**. Proprietary business logic and full production code are intentionally excluded.

---

⭐ If you find this project useful or interesting, feel free to star the repository.
