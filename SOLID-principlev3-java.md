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
![Untitlesd](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/b59797df-ba13-4b3e-834f-a24f0fa382ea)
- The above classes do not obey LSP because you cannot replace the Rectangle base class with its derived class Square. The Square class has extra constraints, i.e., the height and width must be the same. Therefore, substituting Rectangle with Square class may result in unexpected behaviour.
## Why is this principle is required?
- This prevents inheritance from being abused. It assists us in adhering to the “is-a” relationship. Subclasses must also adhere to a contract established by the base class. In this way, it’s similar to Bertrand Meyer’s Design by Contract. It’s easy to think of a circle as a form of an ellipse, yet circles lack two foci or major/minor axes.

## 4. Interface segregation principle:
- According to the interface segregation concept, a client should never be required to implement an interface that it does not use, or to rely on any method that it does not use. So, fundamentally, the interface segregation principles are that you favour small, client-specific interfaces over monolithic, larger interfaces. In other words, forcing the client to rely on something they don’t require is not a good idea. In short, No client should be forced to depend on methods that it does not use.
- Let’s understand it with the help of an example:
- Suppose there’s an interface for a vehicle and a Bike class:
![Untiatled](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/42b03c1d-ae66-49bb-81e0-50134daea506)
- As you can see, a Bike class should not implement the openDoors() method because a bike does not have any doors! To address this, ISP offers to break down the interfaces into several, small coherent interfaces so that no class is required to implement any interfaces (and thus methods) that it does not require.
- After implying the interface segregation principle
![Untitwled](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/95e25998-cb3f-4a13-b00e-5d0441395d4a)
## Why is this principle required?
- The Interface Segregation Principle makes our code more readable and maintainable. We’ve pared down our class implementation to simplify the operations that are required, with no extra or extraneous code. As we only use that method that is required and can leave other methods.







