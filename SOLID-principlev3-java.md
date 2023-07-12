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


