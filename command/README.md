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

## When to use? 


## When not to use? 

