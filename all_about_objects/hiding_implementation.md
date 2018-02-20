## Hiding Implementation

When taking a look at the object concept two parties of programmers can be distinguished. On one side is the *class creator* that defines the class and takes care of its implementation. He creates new data types and maintains the internal workings of those classes. On the other side is the *client programmer*, the class consumer, who uses the class and instantiates objects from it.

The client programmers goal is to collect a toolbox of helpful classes (libraries) and use these to develop a solution to his problem as fast as possible and with the least effort.

The class creators goal is to build a class that only exposes what is necessary and hide everything else.

Both these programmers can be the same physical person, however even in this case it is helpful to make a logical distinction between the user and the creator of a class.

Why hide as much as possible? Several reasons:
* If it is hidden, the client programmer can't use it and if he can't use it, he can't misuse it either. The hidden parts of a class represent the tender insides of the implementation and could be easily corrupted if made public.
* Hiding implementation details also allows the class creator to make changes to the hidden portions without having to worry about breaking contract with the client programmer. If you ever decide to for example optimize your implementation you would not need to worry about the people using your library.
* The simpler the public interface of the class, the more programmers will use.

In any case, in any relationship it is important to have boundaries that are respected by all involved parties. When creating libraries, you actually establish a relationship between yourself and the client programmer. That is why we often state that the public interface is a representation of the contract between a class creator and his clients.

**Access control** prevents client programmers to keep hands off portions they shouldn't touch. Hiding the internals that are not part of the interface that users need, is actually a service to the users. Client programmers can easily see what's important for them and ignore the rest.

C++ uses three keywords called **access modifiers** to set those boundaries in a class:
* `public`: Available to everyone ('+' sign in UML)
* `private`: Only available inside the class itself ('-' sign in UML)
* `protected`: Similar to private, except that subclasses can access these members ('#' sign in UML)

Trying to access members that are not available to you, will result in compile-time errors.

![Hiding implementation - Important for both client and creator[^2]](img/hiding_implementation.gif)

[^2]: Source http://javarevisited.blogspot.be/2010/10/abstraction-in-java.html
