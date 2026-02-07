# 🍳 Rasha Recipes

Rasha Recipes is a Flutter app concept to browse and explore cooking recipes organized by categories.

---

## 📌 Project Description
Helps users discover recipes easily. Each recipe has ingredients, cooking steps, and preparation time. Built using MVC architecture for clean code and separation of concerns.

---

## 🏗 Architecture
- **Model:** Handles data  
- **View:** Displays UI  
- **Controller:** Manages business logic

---

## 📁 Project Structure
lib/
├── models/
│ ├── recipe_model.dart
│ ├── category_model.dart
│ └── user_model.dart
├── controllers/
│ ├── recipe_controller.dart
│ └── category_controller.dart
├── views/
│ ├── screens/
│ │ ├── home_screen.dart
│ │ ├── recipe_details_screen.dart
│ │ └── category_screen.dart
│ └── widgets/
│ ├── recipe_card.dart
│ └── category_item.dart
├── services/
│ └── recipe_service.dart
├── utils/
│ └── constants.dart
└── main.dart

---

## 🧩 Models

### Recipe Model
Holds recipe data: name, cooking time, ingredients, steps.

### Category Model
Represents recipe categories (desserts, main dishes, drinks).

### User Model (Optional)
Represents the app user for favorites or settings.

---

## 🧠 Example Code

**Recipe Model**
```dart
class Recipe {
  final String id;
  final String name;
  final int cookingTime;
  final List<String> ingredients;
  final List<String> steps;

  Recipe({required this.id, required this.name, required this.cookingTime, required this.ingredients, required this.steps});

  factory Recipe.fromJson(Map<String, dynamic> json) => Recipe(
    id: json['id'],
    name: json['name'],
    cookingTime: json['cookingTime'],
    ingredients: List<String>.from(json['ingredients']),
    steps: List<String>.from(json['steps']),
  );

  Map<String, dynamic> toJson() => {
    'id': id,
    'name': name,
    'cookingTime': cookingTime,
    'ingredients': ingredients,
    'steps': steps,
  };
}
class Category {
  final String id;
  final String title;
  Category({required this.id, required this.title});
}
import '../models/recipe_model.dart';

class RecipeController {
  final List<Recipe> recipes = [];
  void addRecipe(Recipe recipe) => recipes.add(recipe);
  List<Recipe> getAllRecipes() => recipes;
}
import 'package:flutter/material.dart';

class HomeScreen extends StatelessWidget {
  const HomeScreen({super.key});
  @override
  Widget build(BuildContext context) {
    return Scaffold(
      appBar: AppBar(title: const Text('Rasha Recipes')),
      body: const Center(child: Text('Recipes List Here')),
    );
  }
}
   ---
##🚀 Features

Browse recipes by category
View recipe details
Clean MVC structure

##🛠 Technologies
Flutter
Dart
MVC Architecture
