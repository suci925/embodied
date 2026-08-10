# About ROS2
## 1.ROS(Robot Operating System) is an opensource ecosystem that provides frameworks,tools,and libraries for building,deploying,running,and maintaining robot applications.
## Frame
### 1.The ROS frameworks is a "pipline" that enables communication between various components of a robot and within the robot itself.It includes message passing,standard interfaces ,and support for multiple programming languages and  platforms.
### 2.ROS consists of the following basic components: 'Node', 'Interfaces(themes,services and anctions)', 'parameters', 'clienr library'.
## Tool
### 1.The tools in ROS help developers build,test and monitor robot systems. They do not add new robot behaviors but make development easier.
### 2.The core toolset provided by ROS enables you to handle the following elements in the development workflow:'Analysis', 'Node Management', 'Introspection', Debugging', 'build', 'Visualization'.
## Capacity
### 1.The capabilities in ROS are ready-to-use software packges that procide general functions for robots,such as operation,motion planning,and perception.These software packages allow developers to add advanced behaviors without starting from scrach.
### 2.ROS offers the following core functions,which can be used out of the box or through supported third-party solutions:'simulation', 'motion planning',' Navigation', 'Control', 'Cognition'.
# NODE 
## 1.Nodes are participants in the ROS2 graph,and the ROS 2 graph commnicates with other nodes using client libraries.Nodes can commnicate with other nodes within the same process, nodes in different processes,or on different machines.Nodes are usually the compiting units in ROS graph;Each node should perform a logical task.
## 2.Nodes can publish to a specified topic to pass data to other nodes ,or subscribe to a specified topic to obtain data from other nodes, They can also act as service clients,allowing other nodes to perform computations on their behalf,or as service sercer to provide functionality to other nodes.For long-runniong computations,a node can act as an action client to have anather node perform it on their behalf,or as an anction sercer to provide functionality to other nodes,Nodes can provide configurable parameter to change bahavior during run-time.
## 3.Nodes are typically complex combinations of pulishers,subscribers,and action clients,all exsiting somiltaneously.
## 4.The connections between nodes are eatablished through a distributed discovery process.

# DISCOVERY
## Discovery of nodes happens automatically through the underlying middleware of ROS2.It can be summarized as follows:
### 1.When a node is started,it advertieses its presence to other nodes on the networks with the same ROS domain(set with the ROS_DOMAIN_ID enviroment variable).Nodes repond to this advertisement with information about themselves so that the appropriate connections can be made the nodes can commnicate.
### 2.Nodes periodically advertise their presence so that connections can be made with new_found entities,even after initial discovery period.
### 3.Nodes advertise to other nodes when they go offline.
### 4.Nodes will only establish connections with other nodes if they have compatible quality of service settings.
