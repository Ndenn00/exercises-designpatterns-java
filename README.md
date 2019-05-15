# exercises-designpatterns-java
A collection of java design patterns and notes for reference

## Creational
### [Factory Methods](./factory/src)
* Creates an instance of several derived classes

### [Singleton](./singleton) 

## Behavioural 
### [Observer](./observer)
* A way of notifying change to a number of classes

### [Strategy](./strategy)
* USe composition over inheritance

## [Decorator](./decorator)


## Read UML 

# Relationships 
![umlRelationships](images/umlRelationships.png)
* Associations - a basic relationship typically named using a verb or verb phrase which reflects the real world problem domain.
* Aggregation - A special type of association. Represents 'part of' Class2 is part of Class1.
* Composition - A special type of aggregation where parts are destroyed when the whole is destroyed.
* Dependency - An object of one class might use an object of another class in the code of a method. If the object is not stored in any field, then this is modeled as a dependency relationship.
* Realization is a relationship between the blueprint class and the object containing its respective implementation level details. This object is said to realize the blueprint class. In other words, you can understand this as the relationship between the interface and the implementing class.
..*For example, the Owner interface might specify methods for acquiring property and disposing of property. The Person and Corporation classes need to implement these methods, possibly in very different ways.






