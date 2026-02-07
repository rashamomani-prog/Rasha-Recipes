# 🍳 Rasha Recipes 

A Flutter application that allows users to browse and explore a variety of cooking recipes organized by categories.

---

## 📌 Project Description
Rasha Recipes App helps users discover different food recipes easily.
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

- class Recipe {
  final String id;
  final String name;
  final int cookingTime;
  final List<String> ingredients;
  final List<String> steps;

  Recipe({
    required this.id,
    required this.name,
    required this.cookingTime,
    required this.ingredients,
    required this.steps,
  });

  factory Recipe.fromJson(Map<String, dynamic> json) {
    return Recipe(
      id: json['id'],
      name: json['name'],
      cookingTime: json['cookingTime'],
      ingredients: List<String>.from(json['ingredients']),
      steps: List<String>.from(json['steps']),
    );
  }

  Map<String, dynamic> toJson() {
    return {
      'id': id,
      'name': name,
      'cookingTime': cookingTime,
      'ingredients': ingredients,
      'steps': steps,
    };
  }
}

-class Category {
  final String id;
  final String title;

  Category({
    required this.id,
    required this.title,
  });
}
-import '../models/recipe_model.dart';

class RecipeController {
  final List<Recipe> recipes = [];

  void addRecipe(Recipe recipe) {
    recipes.add(recipe);
  }

  List<Recipe> getAllRecipes() {
    return recipes;
  }
}

-import 'package:flutter/material.dart';

class HomeScreen extends StatelessWidget {
  const HomeScreen({super.key});

  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text('Rasha Recipes')),
      body: const Center(
        child: Text('Recipes List Here'),
      ),
    );
  }
}

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
