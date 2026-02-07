# 🍳 Rasha Recipes 

A Flutter application that allows users to browse and explore a variety of cooking recipes organized by categories.

---

## 📌 Project Description
The Cooking Recipes App helps users discover different food recipes easily.
Each recipe includes ingredients, cooking steps, and preparation time. The app is designed using the MVC architecture to ensure clean code and separation of concerns.

---

## 🏗 Architecture
This project follows the **MVC (Model-View-Controller)** architectural pattern:

- **Model:** Handles application data and data structures.
- **View:** Responsible for the user interface and user interaction.
- **Controller:** Contains the business logic and connects models with views.

---

## 📁 Project Structure
lib/
├── models/
│ ├── recipe_model.dart
│ ├── category_model.dart
│ └── user_model.dart
│
├── controllers/
│ ├── recipe_controller.dart
│ └── category_controller.dart
│
├── views/
│ ├── screens/
│ │ ├── home_screen.dart
│ │ ├── recipe_details_screen.dart
│ │ └── category_screen.dart
│ │
│ └── widgets/
│ ├── recipe_card.dart
│ └── category_item.dart
│
├── services/
│ └── recipe_service.dart
│
├── utils/
│ └── constants.dart
│
└── main.dart

---

## 🧩 Models
- **Recipe:** Represents a single cooking recipe with ingredients and preparation steps.
- **Category:** Represents recipe categories such as desserts or main dishes.
- **User (Optional):** Represents the user for future features like favorites.

---

## 🚀 Features
- Browse recipes by category
- View recipe details
- Clean and scalable MVC structure

---

## 🛠 Technologies Used
- Flutter
- Dart
- MVC Architecture

---
