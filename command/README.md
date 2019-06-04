# Command Pattern 

The Command design pattern encapsulates commands (method calls) in objects allowing us to issue requests without knowing the requested operation or the requesting object. 
Command design pattern provides the options to queue commands, undo/redo actions and other manipulations.
![CommandImage](../images/commandClassDiagram.gif)

## How? 

The classes participating in the pattern are:
* Command - declares an interface for executing an operation;
* ConcreteCommand - extends the Command interface, implementing the Execute method by invoking the corresponding operations on Receiver. It defines a link between the Receiver and the action.
* Client - creates a ConcreteCommand object and sets its receiver;
* Invoker - asks the command to carry out the request;
* Receiver - knows how to perform the operations;

```
public class RemoteControlTest {  //This is the client 
	public static void main(String[] args) {
		SimpleRemoteControl remote = new SimpleRemoteControl(); //This is the invoker - it is passed a command object 
		Light light = new Light(); // This is the reciever 
		LightOnCommand lightOn = new LightOnCommand(light); // This is a command, that will be passed to the reciever

```

## Why? 
* Completely decouple a client calling a method from the receiving object. 
* View the history of requests made or as you need, undo them.
* Encapsulate all the data you want to send.
* Change the parameters of these requests without violating the open-closed principle.



## When to use? 
Typical uses of the the command pattern are systems that take some piece of computation and pass it as a first class object. 
The client creates the object and calls the execute method on a loosely coupled action. 
These actions can be called on by different threads. 

Imagine a job queue, you add commands at one end and at the other end are threads. Threads remove the command from the queue, call the execute method, 
wait for the call to finish, then discard the command object and retrieve a new one. 

This model can include use cases for: 
* Schedulers
* Thread pools 
* Job queues
