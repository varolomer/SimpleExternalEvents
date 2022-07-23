![alt text](https://github.com/varolomer/RevitExternalEvents/blob/master/RevitModelessWinForm/Assets/Github/Banner.png)

# Revit External Events
This is a tutorial repository which shows how the Revit External Events work in a very fundemantal scenario. Especially for the beginners, it could be very hard to grasp the concept of External Events. That's why I wanted write a very simple plugin, based on the examples from RevitSDK, which exposes the basic functionality without complex workflows like wrappers, abstract objects which makes it hard to understand the basics.

## Why External Events
Revit external events gives us the functionality to have Modeless Forms in Revit. Normally, when we use the commands that implement IExternalCommand, the command has a procedural flow and then returns Result object immediately after its job is done. However, with raising and handling external events we have much more flexibility on how our program and UI works.

## Limitations
Due to the reason that the library is writtten for beginners and in a very basic scenario, this way of dealing with External Events have some limitations:

- Arguments cannot be passed from UI to event handler and vice versa
- When the command has a functionality where it will keep Revit busy for a while, the UI gets unresponsive
- It is not suitable for Asyncronous Pattern. No Task-Based approach

As an important addition, it is extremely tedious to pass event handlers and events to UI instance especially when there will be many External Events. To take care of this issue, there are much better approaches to deal with events like abstract classes which wrap the events properly. To keep this library simple for beginners, this kind of approaches are ignored. There will be another repository for these more advanced approaches.


## Notes
this library is written for beginners. The variable names are long-written, the code-flow is simplified.
