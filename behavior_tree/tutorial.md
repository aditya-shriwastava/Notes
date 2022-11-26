# Tutorial

* BehaviorTree.CPP provides a basic mechanism of dataflow through **port**.
* **Blackboard:**
  + A simple key/value storage shared by all the nodes of the tree.
* **Input port:**
  + A valid input port can be either:
    + A static string that the Node will read and parse.
    + A "pointer" to an entry of the Blackboard, identified by a key. 
