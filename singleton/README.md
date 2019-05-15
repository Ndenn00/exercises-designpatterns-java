# Singleton Pattern

![singletonImage](../images/singletonClassDiagram.gif)

The singleton is a _convention_ that will ensure one and only one object is instantiated for a given class. 
It also offers a global point of access. 

## Why? 
* A class manages a single instance of itself, preventing any other class from creating a new instance on its own. 
* To get an instance, you have to go through the class itself to request its instance. 
* Global access to the class is provided, you can request the instance publicly. 

## How? 
__No public constructor__

__Define a private constructor in your class to stop instantiation of new Singleton__

The singleton object is never instantiated. Instead you request an instance, typically calling a getInstance(). 

## When to use? 
* Objects that you only need one of: thread pools, caches, preferences and registry settings.
** e.g. Logging, drivers for devices such as printers 

## When not to use? 
* When your use case is resource intensive and it gets created on startup, but might not be used. 

## Multithreading 
Two threads can execute a method of the instance, leading to multithreading. We can deal with this in three ways.  
1. If performance isn't critical, do nothing. We can add the synchronised keyword in the method declaration to help solve for this. The clients will just have to wait their turn.
This can slow the application by factor 100 though, be warned.  
2. Move to an eagerly created instance, rather than a lazy one. 
Create an instance of your singleton using a static initializer in the Singleton class. This is the thread safe example in /src. 
This ensures that the one instance is created, and will always be threadsafe. 
3. Double checked locking checks if the instance is created, and if not then you synchronize.
The volatile keyword ensures that multiple threads handle the unique instance variable correctly when it is being initialized to the Singleton instance. 
