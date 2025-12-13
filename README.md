# 📚 Library Management System

A comprehensive Java-based library management system built with Object-Oriented Programming principles. This system provides a complete solution for managing library inventory (books and magazines) and client records through an intuitive console interface.

## ✨ Features

### Item Management
- ✅ **Create** books and magazines with detailed information
- 📖 **Read** and view item details
- ✏️ **Update** existing items (title, pages, author)
- 🗑️ **Delete** items from the library

### Client Management
- 👤 **Register** new library clients
- 📋 **View** client information
- ✏️ **Update** client details
- ❌ **Remove** clients from the system

### Smart Features
- 🔒 Custom exception handling for data integrity
- ✅ Input validation (integers, alphabetic strings, email format)
- 🎯 Type-safe operations with inheritance
- 📦 Organized package structure

## 🏗️ Project Structure

```
Library/
├── Entities/              # Domain models
│   ├── LibraryItem.java   # Abstract base class for items
│   ├── Book.java          # Book entity with author
│   ├── Magazine.java      # Magazine entity
│   └── Client.java        # Library client entity
│
├── Management/            # Business logic layer
│   └── Library.java       # Core library operations
│
├── UI/                    # User interface layer
│   ├── Menu.java          # Abstract menu base class
│   ├── MainMenu.java      # Main application menu
│   ├── ItemMenu.java      # Item management menu
│   └── ClientMenu.java    # Client management menu
│
├── Helpers/               # Utility classes
│   └── UserInput.java     # Input validation utilities
│
├── Exceptions/            # Custom exceptions
│   ├── ItemAlreadyExistsException.java
│   ├── ItemNotExistException.java
│   ├── ClientAlreadyExistsException.java
│   └── ClientNotExistException.java
│
└── Main.java              # Application entry point
```

## 🚀 Getting Started

### Prerequisites
- **Java Development Kit (JDK)** 8 or higher
- A terminal/command prompt
- (Optional) An IDE like VS Code, IntelliJ IDEA, or Eclipse

### Installation

1. **Clone the repository**
   ```bash
   git clone https://github.com/mohamedabdelhaq-123/Library.git
   cd Library
   ```

2. **Compile the project**
   ```bash
   javac -d bin Main.java Entities/*.java Management/*.java UI/*.java Helpers/*.java Exceptions/*.java
   ```

3. **Run the application**
   ```bash
   java -cp bin Main
   ```

### Quick Start Script

**Linux/Mac (run.sh):**
```bash
#!/bin/bash
javac -d bin Main.java Entities/*.java Management/*.java UI/*.java Helpers/*.java Exceptions/*.java
java -cp bin Main
```

**Windows (run.bat):**
```batch
@echo off
javac -d bin Main.java Entities/*.java Management/*.java UI/*.java Helpers/*.java Exceptions/*.java
java -cp bin Main
```

## 📖 Usage

### Main Menu
```
=====>Main Menu<=====
1- Item Menu
2- Client Menu
0- Exit
```

### Item Menu Operations
```
=====>Item Menu<=====
1- Create Item
2- Read Item
3- Update Item
4- Delete Item
0- Back to Main Menu
```

### Example: Adding a Book
1. Select `1` from Main Menu (Item Menu)
2. Select `1` (Create Item)
3. Select `1` (Create Book)
4. Enter Book ID: `101`
5. Enter Name: `JavaProgramming`
6. Enter Author: `JamesGosling`
7. Enter Number of Pages: `500`

## 🛠️ Technical Details

### Design Patterns
- **Inheritance**: `Book` and `Magazine` extend `LibraryItem`
- **Polymorphism**: Menu system using abstract base class
- **Encapsulation**: Private fields with public getters/setters
- **Exception Handling**: Custom exceptions for business logic

### Input Validation
- **Integer validation**: Ensures numeric input for IDs and pages
- **Alphabetic validation**: Ensures text-only input for names
- **Email validation**: Regex pattern matching for client emails
- **Error handling**: User-friendly error messages and retry logic

### Key Classes

| Class | Purpose |
|-------|---------|
| `LibraryItem` | Abstract base for all library items |
| `Book` | Represents a book with author information |
| `Magazine` | Represents a magazine publication |
| `Client` | Represents a library patron |
| `Library` | Manages collections of items and clients |
| `UserInput` | Provides validated input methods |

## 🎯 Object-Oriented Principles

- **Abstraction**: Abstract `Menu` and `LibraryItem` classes
- **Inheritance**: Books and Magazines inherit from LibraryItem
- **Polymorphism**: Different menu implementations
- **Encapsulation**: Private fields with controlled access

## 🔧 Development

### Adding a New Item Type
1. Create a new class extending `LibraryItem` in `Entities/`
2. Implement required abstract methods
3. Add creation logic in `ItemMenu.java`
4. Update the menu options

### Adding New Validation
1. Add static method to `UserInput.java`
2. Use appropriate regex pattern
3. Include error message for invalid input

## 🤝 Contributing

Contributions are welcome! Please feel free to submit a Pull Request.

1. Fork the project
2. Create your feature branch (`git checkout -b feature/AmazingFeature`)
3. Commit your changes (`git commit -m 'Add some AmazingFeature'`)
4. Push to the branch (`git push origin feature/AmazingFeature`)
5. Open a Pull Request

## 📝 License

This project is open source and available under the [MIT License](LICENSE).

## 👨‍💻 Author

**Mohamed Abdelhaq**
- GitHub: [@mohamedabdelhaq-123](https://github.com/mohamedabdelhaq-123)

## 🙏 Acknowledgments

- Inspired by real-world library management needs
- Built as a demonstration of OOP principles in Java
- Designed with scalability and maintainability in mind

---

⭐ **Star this repository if you find it helpful!**

📫 **Questions or suggestions?** Feel free to open an issue!
