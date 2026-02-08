# CaptapApp

A scalable, cross-platform **Pharmacy Management System** built with **Flutter**
(Mobile • Tablet • Desktop)

---

## 📌 Project Overview

CaptapApp is a multi-platform pharmacy management system designed and implemented using Flutter to support **real-world pharmacy business workflows** across mobile, tablet, and desktop devices.

This repository focuses on showcasing **architecture, design decisions, scalability strategies, and development practices**. The full production codebase is not included due to **confidentiality and code ownership constraints**.

---

## 🚀 Key Features

* Modular and scalable architecture using **Clean Architecture**
* Predictable and maintainable state management with **BLoC**
* Local database integration using **sqflite**
* Fully responsive UI for:

  * 📱 Mobile
  * 📊 Tablet
  * 🖥️ Desktop
* Real device integrations:

  * QR Code scanning
  * Barcode scanning
  * Camera access & permissions
  * Location and address handling
* Multi-language support (Arabic, English, Turkish)

---


## 🧠 Architecture & Design Philosophy

CaptapApp was architected with **long-term scalability, maintainability, and clarity** in mind before any implementation started.

### 🔹 Clean Architecture

The project is structured into three main layers:

* **Presentation Layer**
  UI components + BLoC for state handling

* **Domain Layer**
  Business logic, use cases, and core rules

* **Data Layer**
  Local & remote data sources, repositories, and API implementations

This separation ensures:

* Minimal coupling between layers
* Easy testing and refactoring
* Smooth expansion with new modules (Inventory, Suppliers, Reports, etc.)

---

## 🔄 State Management (BLoC)

State management is handled using **BLoC**, providing:

* Clear and predictable state transitions
* Centralized loading & error handling
* Decoupling between UI and business logic

Use cases are **injected** into BLoCs instead of being instantiated internally, ensuring clean dependency flow and improved testability.

![BLoC & UseCases](screenshots/Screenshot%20\(1493\).png)

---

## 🌐 Networking Layer

Networking is implemented using **Dio** with a clean and extensible setup:

* Centralized API configuration
* Request & response validation
* Interceptors for:

  * Logging
  * Error handling
  * Request status monitoring

Abstract classes are used to define RESTful API contracts and allow method reuse across multiple services.

![Dio Interceptors](screenshots/Screenshot%20\(1492\).png)
![Abstract API](screenshots/Screenshot%20\(1491\).png)

---

## ⚖️ Object Comparison & Performance

To ensure accurate state comparison and avoid unnecessary object recreation, **Equatable** is used:

* Efficient object comparison
* Improved performance in BLoC state updates

![Equatable](screenshots/equtable.PNG)

---

## 🔌 Dependency Injection

Dependency Injection is implemented using a **Service Locator** pattern:

* Centralized object creation
* Lazy initialization when required
* Clean dependency management across layers

![Dependency Injection](screenshots/Screenshot%20\(1490\).png)

---

## 📱 Navigation & Routing

Navigation is handled using a centralized `generateRoute` approach:

* Clean route definitions
* Decoupled navigation logic
* Easy scalability for future modules

![Generate Route](screenshots/Screenshot%20\(1494\).png)

---

## 📐 Responsive UI Strategy

The UI includes **380+ screens**, all converted from Figma into a fully responsive Flutter interface.

### ❌ Why ScreenUtil Was Not Enough

ScreenUtil showed limitations when:

* System font size increased (accessibility issues)
* Layouts were rendered on tablets & desktops
* Scaling became inconsistent across platforms

### ✅ Custom Config & Size Management

A **custom Config / SizeConfig solution** was implemented instead:

* Defined clear breakpoints (Mobile / Tablet / Desktop)
* Centralized spacing, padding, and typography rules
* Full respect for system font scaling
* Predictable layouts across all platforms

![Size Config](screenshots/size_config.PNG)
![Responsive Layouts](screenshots/responsive.PNG)

---

## 🌍 Localization & Accessibility

CaptapApp supports **three languages**:

* Arabic (RTL support)
* English
* Turkish

Localization is handled using a centralized **AppLocalization** system:

* Clean language switching
* Easy addition of new languages
* Separation of UI and translation resources

![App Localization](screenshots/app_localization.PNG)

---

## 🎨 Theme & Color Management

All application colors are managed using a **ColorManager** implemented as an **abstract class with static properties**:

* No hardcoded colors in UI widgets
* Consistent theming across the entire app
* Easy brand and theme updates

![Color Manager](screenshots/abstract_static_color_manager.PNG)

---

## 🧠 Planning Before Coding

Before development started:

* Functional & non-functional requirements were defined
* Scalability paths were planned
* Core technical decisions were finalized early

This approach resulted in a **predictable, maintainable, and production-ready codebase**.

---

## 🎯 Client-Focused Development

Throughout implementation:

* Real pharmacy workflows guided feature design
* UI/UX decisions matched real usage scenarios
* Device permissions were handled contextually across platforms

---

## 📸 Cross-Platform Mockup

![Captap Mockup](screenshots/captap_mockup.png)

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

This repository is intended for **portfolio and architectural demonstration purposes only**. Proprietary business logic and full production code are intentionally excluded.

⭐ If you find this project useful or interesting, feel free to star the repository.
