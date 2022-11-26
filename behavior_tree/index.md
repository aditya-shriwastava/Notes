# Behavior Tree

* Mathematical model of plan execution used in robotics.
* Provides ability to create very complex tasks as composed of simple tasks without worring about how the simple tasks are implemented.

## Behavior Tree CPP Library
> [Github](https://github.com/BehaviorTree/BehaviorTree.CPP), [Website](https://www.behaviortree.dev/)

* Fast, easy to use and flexible.
* It makes asynchronous Actions, a first-class citizen.
* Trees are created at run-time, using an interpreted language (based on XML).
* It includes a logging/profiling infrastructure that allows the user to visualize, record, replay and analyze state transitions.
* You can link statically your custom TreeNodes or convert them into plugins which are loaded at run-time.

### What is a behavior tree?

* A Behavior Tree (BT) is a way to structure the switching between different **tasks** in an autonomous agent.
* Think about the Nodes of the tree as a set of building blocks.
* These blocks are implemented in C++ and are "composable": in other words, they can be "assembled" to build behaviors.
* Main advantages of behavior tree:
  * They are intrinsically Hierarchical.
  * Their graphical representation has a semantic meaning.
  * They are more expressive.
* A "good" software architecture should have the following characteristics:
  * Modularity.
  * Reusability of components.
  * Composability.
  * Good separation of concerns.

1. [Basic Concepts](basic_concepts.md)
2. [Tutorial](tutorial.md)
