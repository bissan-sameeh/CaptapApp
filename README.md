# CaptapApp

**A scalable, cross-platform Pharmacy Management System built with Flutter**  
(Mobile • Tablet • Desktop)

---

## 📌 Project Overview

CaptapApp is a **multi-platform pharmacy management system** designed and implemented using **Flutter**, intended to serve business workflows across **mobile, tablet, and desktop** devices.  
This repository showcases the project’s architecture, design decisions, and code structure — not the full original production code due to confidentiality.

---

## 🚀 Key Features

- Modular architecture following **Clean Architecture**
- Organized state management using **BLoC**
- Local database integration with **sqflite**
- Responsive UI adapted for:
  - 📱 Mobile
  - 📊 Tablet
  - 🖥️ Desktop
- Integration of real device features:
  - QR code scanning
  - Barcode scanning
  - Camera access permissions
  - Location/address handling

---

## 🧠 Architecture & Design

CaptapApp was architected with **scalability & maintainability** in mind:

### 🔹 Clean Architecture
The project separates:
- **Presentation Layer** (UI + BLoC)
- **Domain Layer** (business logic)
- **Data Layer** (legacy/local & remote data sources)

This enables easy expansion with new modules (e.g., Inventory, Suppliers, Reporting) with minimal changes to core logic.

---

## 📐 State Management

State is handled using **BLoC**, providing:
- Clear state transition logic
- Centralized error/loading handling
- Predictable UI updates

---

## 💾 Local Storage

Used **sqflite** for structured and scalable local storage, handling:
- Multiple relational tables
- Offline data access
- Data caching strategies

---

## 🌐 Networking

Networking is implemented using **Dio** with:
- Centralized API structure
- Interceptors for logging and error handling
- Request/response validation

---

## 📱 Responsive UI Strategy

The design includes **over 380 screens** converted from Figma into a responsive Flutter UI.

### 🧩 Why ScreenUtil Was Not Enough

Although **ScreenUtil** was initially used for scaling, it showed limitations when:
- System font size increased (accessibility needs)
- Layouts were rendered on larger screens (tablet & desktop)

### 🛠️ Custom Config Class

To improve responsiveness and accessibility, a **Custom Config Class** was created to:
- Control layout breakpoints
- Manage spacing, padding & device-specific sizing
- Ensure consistent UI behavior on all platforms

This approach enhanced:
- Accessibility with larger fonts
- Predictable responsive layouts
- Long-term UI maintainability

---

## 🧠 Planning Before Coding

Before development began:
- The system’s **functional and non-functional requirements** were mapped out
- Future modules and scalability paths were architected
- Core decisions (state management, data persistence, networking) were planned upfront

This led to a **maintainable and predictable codebase** for large scale business systems.

---

## 🎯 Client-Focused Development

Throughout the implementation:
- Real business workflows guided feature design
- UI/UX decisions matched actual pharmacy usage scenarios
- Device permissions were handled contextually across platforms

---

## 📸 Screenshots / Demos

Screenshots and GIFs of key screens are included under the `/screenshots` folder for easier visual context and portfolio presentation.

---

## 🛠️ Built With

- **Flutter**
- **Dart**
- **BLoC**
- **Clean Architecture**
- **sqflite**
- **Dio**
- Device integrations (QR/Barcode/Camera/Location)



# Run app
flutter run
