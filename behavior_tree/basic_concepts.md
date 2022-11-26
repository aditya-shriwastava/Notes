# Basic Concepts

- A signal called **tick** is sent to the root of the tree and propagates through the tree until it reaches a leaf node.
- Any TreeNode that receives a tick signal executes its callback. This callback must return either:
  - SUCCESS
  - FAILURE: This means action needs more time to return a valid result.
  - RUNNING

## Type of nodes

* TreeNode
  + **DecoratorNode:** Among other things, it may alter the result of the children or tick it multiple times.
  + **ControlNode:** Usually, ticks a child based on the result of its siblings or/and its own state.
    + **SequenceNode**
    + **FallbackNode**
  + **LeafNode**
    + **ConditionNode:** Should not alter the system. Shall not return RUNNING.
    + **ActionNode:** This is the Node that "does something"
      + ActionNodes, we may further distinguish between synchronous and asynchronous nodes .

The user must create his/her own ActionNodes and ConditionNodes (LeafNodes); this library helps you to compose them easily into trees.

Trees can be created and composed at run-time, more specifically, at deployment-time, using an XML base scripting language.

**Blackboard:** A key/value storage shared by all the Nodes of a Tree.

**Ports:** Mechanism that Nodes can use to exchange information between each other.

Custom Nodes can be created using inheritance or function pointer.
