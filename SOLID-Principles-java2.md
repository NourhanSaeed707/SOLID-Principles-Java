# The Reason for SOLID Principles:
- What is SOLID and how does it help us write better code? Simply put, Martin and Feathers' design principles encourage us to create more maintainable, understandable, and flexible software. Consequently, as our applications grow in size, we can reduce their complexity and save ourselves a lot of headaches further down the road!

## 1. Single Responsibility Principles:
- Let's begin with the single responsibility principle. As we might expect, this principle states that **a class should only have one responsibility. Furthermore, it should only have one reason to change.**
- **How does this principle help us to build better software?** Let's see a few of its benefits:
1. Testing – A class with one responsibility will have far fewer test cases.
2. Lower coupling – Less functionality in a single class will have fewer dependencies.
3. Organization – Smaller, well-organized classes are easier to search than monolithic

## 2. open-closed principle:
- **classes should be open for extension but closed for modification. In doing so, we stop ourselves from modifying existing code and causing potential new bugs** in an otherwise happy application.
Of course, **the one exception to the rule is when fixing bugs in existing code.**
Let's explore the concept with a quick code example. As part of a new project, imagine we've implemented a Guitar class.
![Untitled](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/4baef784-bbc1-4bd8-a7dc-dac7daeac3f8)

- We launch the application, and everyone loves it. But after a few months, we decide the Guitar is a little boring and could use a cool flame pattern to make it look more rock and roll.
- At this point, it might be tempting to just open up the Guitar class and add a flame pattern — but who knows what errors that might throw up in our application.
Instead, **let's stick to the open-closed principle and simply extend our Guitar class**:
![Untiteled](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/387bb1c1-bdd3-4084-a67d-afc2e8c47b2e)
- By extending the Guitar class, we can be sure that our existing application won't be affected.

## 3. Liskov Substitution:
- Next on our list is Liskov substitution, which is arguably the most complex of the five principles. Simply put, **if class A is a subtype of class B, we should be able to replace B with A without disrupting the behavior of our program.**
Let's jump straight to the code to help us understand this concept:
![Untitledw](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/83b79645-e841-4d41-91ae-deb17a0f750f)
- Above, we define a simple Car interface with a couple of methods that all cars should be able to fulfill: turning on the engine and accelerating forward.
- Let's implement our interface and provide some code for the methods:
![Untitlede](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/784fc83c-f35f-446a-a02a-6ccdafc788c7)
- As our code describes, we have an engine that we can turn on, and we can increase the power.
- But wait — we are now living in the era of electric cars:
![Unwtitledw](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/fd4dc15b-7b97-4e00-9433-25d7b0d9b11d)
- By throwing a car without an engine into the mix, we are inherently changing the behavior of our program. This is a blatant violation of Liskov substitution and is a bit harder to fix than our previous two principles.
One possible solution would be to rework our model into interfaces that take into account the engine-less state of our Car.

## 4. Interface Segregation:
- The I  in SOLID stands for interface segregation, and it simply means that **larger interfaces should be split into smaller ones. By doing so, we can ensure that implementing classes only need to be concerned about the methods that are of interest to them.**
For this example, we're going to try our hands as zookeepers. And more specifically, we'll be working in the bear enclosure.
Let's start with an interface that outlines our roles as a bear keeper:
![Untitled](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/4aeaed32-be68-40ad-bf49-62baabbf3fcd)
- As avid zookeepers, we're more than happy to wash and feed our beloved bears. But we're all too aware of the dangers of petting them. Unfortunately, our interface is rather large, and we have no choice but to implement the code to pet the bear.
- **Let's fix this by splitting our large interface into three separate ones:**
![Untitsled](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/7e0256d2-8d32-4b64-a373-c0a89ca90643)
- Now, thanks to interface segregation, we're free to implement only the methods that matter to us:
![Untitled2](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/510c127c-34d8-4909-821c-01387adcd820)
- And finally, we can leave the dangerous stuff to the reckless people:
![Untitlewd](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/592e453a-6fb0-4d23-8c2f-6a75c8a18933)
- Going further, we could even split our BookPrinter class from our example earlier to use interface segregation in the same way. By implementing a Printer interface with a single print method, we could instantiate separate ConsoleBookPrinter and OtherMediaBookPrinter classes.

## 5. Dependency Inversion:
- **The principle of dependency inversion refers to the decoupling of software modules. This way, instead of high-level modules depending on low-level modules, both will depend on abstractions.**
- To demonstrate this, let's go old-school and bring to life a Windows 98 computer with code:
![Untitled](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/4d154efe-c9fe-482b-a6a1-8a23bf6c60ef)
- But what good is a computer without a monitor and keyboard? Let's add one of each to our constructor so that every Windows98Computer we instantiate comes prepacked with a Monitor and a StandardKeyboard:
![Untitlwed](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/2e66f2f7-63c9-4136-bb49-60e395d11037)
- This code will work, and we'll be able to use the StandardKeyboard and Monitor freely within our Windows98Computer class.
- Problem solved? Not quite. **By declaring the StandardKeyboard and Monitor with the new keyword, we've tightly coupled these three classes together.**
- Not only does this make our Windows98Computer hard to test, but we've also lost the ability to switch out our StandardKeyboard class with a different one should the need arise. And we're stuck with our Monitor class too.
- Let's decouple our machine from the StandardKeyboard by adding a more general Keyboard interface and using this in our class:
![Untiwtled](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/4be43645-3701-47ad-8baa-99df15d09c35)
- Here, we're using the dependency injection pattern to facilitate adding the Keyboard dependency into the Windows98Machine class.
- Let's also modify our StandardKeyboard class to implement the Keyboard interface so that it's suitable for injecting into the Windows98Machine class:
![Untitledw](https://github.com/NourhanSaeed707/SOLID-Principles-Java/assets/64387352/8d6c189f-dd46-4374-bcda-8feb1f0489ec)
- Now our classes are decoupled and communicate through the Keyboard abstraction. If we want, we can easily switch out the type of keyboard in our machine with a different implementation of the interface. We can follow the same principle for the Monitor class.











