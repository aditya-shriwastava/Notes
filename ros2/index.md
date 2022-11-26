# ros2

* **underlay:** core ros2 workspace
* **overlay:** workspaces on top of core workspace

**ROS_DOMAIN_ID varible:**
  * In DDS, the primary mechanism for having different logical networks share a physical network is known as the Domain ID
  * ROS 2 nodes on the same domain can freely discover and send messages to each other, while ROS 2 nodes on different domains cannot.
  * All ROS 2 nodes use domain ID 0 by default.
  * [Safe number] simply choose a domain ID between 0 and 101, inclusive.

**ROS_LOCALHOST_ONLY varible**
  * ROS_LOCALHOST_ONLY environment variable allows you to limit ROS 2 communication to localhost only.

1. [ROS Graph](ros_graph.md)
2. [Client libraries](client_libraries.md)
