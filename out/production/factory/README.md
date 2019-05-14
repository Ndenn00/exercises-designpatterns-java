# Factory Pattern 

The Factory Pattern defines an interface for creating an object, but lets subclasses decide which class to instantiate. 
Factory methods let a class defer instantiation to subclasses. 

![Simple Factory](https://www.oodesign.com/images/stories/factory%20implementation.gif)

## How? 

* The client needs a product, but instead of creating it directly using the new operator, it asks the factory object for a new product, providing the information about the type of object it needs.
* The factory instantiates a new concrete product and then returns to the client the newly created product(casted to abstract product class).
* The client uses the products as abstract products without being aware about their concrete implementation.

## Why? 
* Creates objects without exposing the instantiation logic to the client.
* Refers to the newly created object through a common interface

## When to use? 
* When the implementation of an interface or an abstract class is expected to change frequently
* When the current implementation cannot comfortably accommodate new change
* When the initialization process is relatively simple, and the constructor only requires a handful of parameters


## When not to use? 
And factories become obsolete when you introduce IoC framework, because IoC is just a kind of factory. 
And many IoC frameworks are able to create implementations of specific factories.

# Achieving the Dependency Inversion Principle 
This principle suggests that high-level components should not depend on low-level components; rather, they should both depend on abstractions. 
The factory method places an abstraction between the client and producer, ensuring loose coupling between the two.
To do this, here a re a few points to keep in mind; 
* No variable should hold a reference to a concrete class.
* No class should derive from a concrete class. 
* No mehid should override an implemented method of any of its base classes (if you override an implemented mehtod then your base class wasn't really an abstraction inn the first place). 