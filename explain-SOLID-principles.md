# What are the SOLID principles in Java?
- **SOLID**  principles are object-oriented design concepts relevant to software development. SOLID is an acronym for five other class-design principles: **S**ingle Responsibility Principle, **O**pen-Closed Principle, **L**iskov Substitution Principle, **I**nterface Segregation Principle, and **D**ependency Inversion Principle.
- SOLID is a structured design approach that ensures your software is modular and easy to maintain, understand, debug, and refactor. Following SOLID also helps save time and effort in both development and maintenance. SOLID prevents your code from becoming rigid and fragile, which helps you build long-lasting software.

# Examples:
## 1. Single responsibility principle:
- Every class in Java should have a single job to do. To be precise, there should only be one reason to change a class. Here’s an example of a Java class that does not follow the single responsibility principle (SRP):
![s](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/065e8e47-4e98-404b-a992-afa8b93aebc6)

- The **Vehicle** class has three separate responsibilities: reporting, calculation, and database. By applying SRP, we can separate the above class into three classes with separate responsibilities.

## 2. Open-closed principle:
- Software entities (e.g., classes, modules, functions) should be open for an extension, but closed for modification.
- Consider the below method of the class VehicleCalculations:
  ![o](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/c43f893f-af7c-4120-b7ac-87ee83e99570)

- Suppose we now want to add another subclass called **Truck**. We would have to modify the above class by adding another if statement, which goes against the Open-Closed Principle.
A better approach would be for the subclasses **Car** and **Truck** to override the calculateValue method:
![Untitled](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/a205b609-43d1-4145-9de9-726e394fe62e)

- Adding another **Vehicle** type is as simple as making another subclass and extending from the Vehicle class.

## 3. Liskov substitution principle:
- **The Liskov Substitution Principle (LSP)** applies to inheritance hierarchies such that derived classes must be completely substitutable for their base classes.

Consider a typical example of a **Square** derived class and **Rectangle** base class:
![Untitled3](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/5dda1993-b1be-4b30-970e-9e2efd72f2d7)

- The above classes do not obey LSP because you cannot replace the **Rectangle** base class with its derived class **Square**. The **Square** class has extra constraints, i.e., the height and width must be the same. Therefore, substituting **Rectangle** with **Square** class may result in unexpected behavior.

## 4. Interface segregation principle:
- **The Interface Segregation Principle (ISP)** states that clients should not be forced to depend upon interface members they do not use. In other words, do not force any client to implement an interface that is irrelevant to them.

Suppose there’s an interface for vehicle and a **Bike** class:
![Untitledw](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/cf8fbd1e-c8e6-4e7d-8a93-3d04c9ce6eed)






