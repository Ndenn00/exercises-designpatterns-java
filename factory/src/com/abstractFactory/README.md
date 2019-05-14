# Abstract Factory

The benefit is trying to avoid the idea of adding code to existing classes in order to make them support encapsulating more general information. 
Take the case of a information manager which manages phone number. Phone numbers have a particular rule on which they get generated depending on areas and countries. 
If at some point the application should be changed in order to support adding numbers form a new country, the code of the application would have to be changed and it would become more and more complicated.

In order to prevent it, the Abstract Factory design pattern is used. Using this pattern a framework is defined, which produces objects that follow a general pattern and at runtime this factory is paired with any concrete factory to produce objects that follow the pattern of a certain country. 
In other words, the Abstract Factory is a super-factory which creates other factories (Factory of factories).

[abstractFactoryImage](https://github.com/Ndenn00/exercises-designpatterns-java/blob/master/factory/src/com/abstractFactory/abstract-factory-pattern.png?raw=true)

## How?

## Why?
* Add new factories without breaking OCP 
* Creates different types of objects  (products) 
* A factory now represents a "family" of objects that it can create
* Factories may have more than one factory method (they can parameterise somehow)

## When to use? 
* Pluralsight uses 
* The system needs to be independent from the way the products it works with are created.
* The system is or should be configured to work with multiple families of products.
* A family of products is designed to work only all together.
* The creation of a library of products is needed, for which is relevant only the interface, not the implementation, too.

## When not to use? 



