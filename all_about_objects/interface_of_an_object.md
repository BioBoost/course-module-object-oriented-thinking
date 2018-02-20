## Interface of an Object

Aristotle was one of the first to study the concept of *type*. He spoke of *the class of fishes and the class of birds*. The idea is that each object is unique (because of their state) but is also part of a class of objects that share characteristics and behavior.

The fundamental keyword *class* was first used in Simula-67, the first object oriented programming language, and allowed for the creation of new types in the program.

The number of objects that can be instantiated from a class is only limited by the memory available in the system the program is running on. Each object has its own state (contained within its data members) and identity.

These objects can then be manipulated (by sending them messages) as if they were the elements from the problem that is being solved.

Objects satisfy the requests that are being send to them (ex. draw something on the screen, complete a bank transaction, download a file from the Internet, ...). In practice, a *contract* is created between the creator of the class and the user of the class, which defines what messages can be send to a certain class of objects. This contract is realized by the **public interface** of the objects. In other words the interface of a class establishes what requests you can make to its objects.

There must however be code somewhere to satisfy the requests. This along with the hidden data comprises the *implementation* of the class.

So summarized: a type (class) has a method associated with each the possible requests (the interface) that can be made to the objects of that class. When a message is send to an object, the corresponding method is called, and the object figures out what to by executing the code that forms the implementation of that method.

Lets take a look at a simple example such as a light bulb. It might be represented as shown below.

![A UML class diagram of a light bulb](https://www.lucidchart.com/publicSegments/view/c41c9a49-31a1-48ba-8552-00a06f6da300/image.png)

The diagram above follows the UML standard (Unified Modeling Language). The diagram consists of three parts:

* The top box shows the **name of the class**. In this case Light. Note how the classname begins with a capital letter and is in the singular form.
* Below that is a list of **attributes**. They contain the characteristics or state of the objects that will be created from the class.
* Last is the box with the **methods** that are available for the class.

Except for the name of the class, the other parts of the diagram are optional and are only added when useful.

The minus '-' sign in front of the attributes state that these are private and cannot be accessed from outside the objects themselves. The plus '+' sign in front of the methods states that they are public and can be called by other type of objects.

Note that the interface of the class only consists of the public portions of the methods and attributes. The methods and attributes that are private are not considered part of the **public interface** of the class. Because of this, some programmers will leave out the private parts of the class from the UML class diagram, as they are considered private details to the actual implementation of the class
