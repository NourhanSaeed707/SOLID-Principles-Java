# Benefits of using SOLID principles:
- When you use all the principles of S.O.L.I.D in a combined manner, it becomes easier for you to develop software that can be managed easily.
- **Clean:** SOLID principles make code clean and standard code.
- **Maintainable:** with the help of SOLID principles our code becomes more manageable and easy to maintain.
- **Scalable:** Easy to refactor or change code.
- **Redundancy:** SOLID principles avoid redundant code.
- **Testable:** can be easily unit tested.
- **Readable:** SOLID principles make the code easy and readable.
- **Independent:** code becomes independent by reducing dependencies.
- **Reusable:** code becomes reusable.
## 1. Single responsibility principle:
- According to the single responsibility principle, each Java class must perform only one function. Multiple capabilities in a single class mashup the code, and any changes made to the code may influence the entire class. It specifies the code and makes it simple to maintain.
- Let’s understand this by using an example:
- Suppose we have a class FinalExam that has 3 methods that perform 3 operations **AddQuestion()**, **ExpectedAnswer()**, **Marksdistribution()**. Now all these 3 methods perform different actions. By using the single responsibility principle, we can separate these functionalities into three separate classes to fulfil the goal of the principle.
  ![Untitled](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/80ca1e49-45f2-4235-bea6-01f954a0ffe3)
- The point of implementing the Single responsibility principle is not that a class can’t have more than one method but it’s -recommended to use a single method for each class so that multiple capabilities in a single class don’t mash up the code, and any changes made to the code may influence the entire class. Using a single responsibility principle makes code easy to maintain.
![Untitlsed](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/566c4f76-4b30-4ab1-8618-3f4bbec29614)

## Why is this Principle Required?
- Testing is made easier when the Single Responsibility Principle is implemented. The class will have fewer test cases with a single responsibility. Because there is less functionality, there are fewer dependencies on other classes. Because smaller, well-purposed classes are easier to search, it leads to better code organization.

## 2. Open-Closed Principle:
- flawlessly without the expectation that it will be changed in the future. As a result, **the class should stay closed to alteration, but it should be possible to extend it.** Extending the class can be done in a variety of ways, including

- **Inheriting from class.**
- **Overwriting the required behaviour from the class.**
- **Extending certain behaviour of the class.**

- Let’s understand it by using an example:
- Suppose, **StudentInfo** is a class and it has the method **Streamname()** that returns the name of the stream.
![Untitwled](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/3cb32053-33b9-452c-9b4e-764f84f640db)
- If we want to add another subclass named arts, simply, we add one more if statement that violates the open-closed principle. The only way to add the subclass and achieve the goal of principle is by overriding the **Streamname()** method, as we have shown below.

![Untitlaed](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/d9a96856-71c7-43d2-94f7-340e67753ed0)

## Why is this principle required?
- Because classes may come from third-party libraries, OCP is essential. We should be able to extend those classes without having to worry about whether or not the base classes will be able to support our expansions. However, inheritance may result in subclasses that are dependent on the implementation of the base class. The use of interfaces is recommended to avoid this. Loose coupling occurs as a result of the added abstraction.

## 3. Liskov substitution principle:
- Barbara Liskov proposed the Liskov Substitution Principle (LSP). It pertains to inheritance in the sense that derived classes must be 100% interchangeable with their base classes. To put it another way, if class A is a subtype of class B, we should be able to substitute B with A without affecting the program’s behaviour.
- It goes beyond the open-close principle to look at how a superclass and its subclasses behave. Unless there is a compelling reason to do otherwise, we should build the classes to preserve the property. Let’s understand it with an example:




