## What is abstraction

The concept of abstraction is to actually **know as little as possible**. All you need to know are the things that are important to you.

> The essence of abstractions is preserving information that is relevant in a given context, and forgetting information that is irrelevant in that context.
>
> John V. Guttag (2013-01-18)

Consider the real-life example of a washing machine. You can perfectly use a washing machine without understanding its internals. All you need to know is the interface it exposes:
* the hole to put the soap in
* the connection to connect the water hose to
* what buttons select the washing program
* a turning knob to select the temperature
* the extension cord to provide it with electricity

As a user of the washing machine you have no idea of the internal workings: what motor is being used, how is the machine heating the water, what microcontroller is used, what's the type of the display, how is the power supply protected, ...

Abstracting things allows us to establishing a level of complexity on which a person interacts with a system. The more complex details are hidden below the current level. The user works with an idealized interface (usually well defined) and can add additional levels of functionality that would otherwise be too complex to handle.

Take for example a programmer that is developing a calculator application. This programmer might not be interested in the way numbers are represented in the underlying hardware (e.g. whether they're 16 bit or 32 bit integers). The boundary where those details have been suppressed, we can state that they have been abstracted away. The programmer now just has numbers with which he can work.
