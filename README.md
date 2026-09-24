# Campus Cable Network Management System

## Project Overview

**Campus Cable Network Management System** is a console-based C++ project designed to represent and manage a campus-wide cable/network infrastructure using graph-based concepts.

In this project, campus locations are represented as **nodes**, while cable connections between locations are represented as **edges**.

Each cable connection stores:

* Cable length
* Installation/connection cost
* Maximum bandwidth capacity
* Current bandwidth load
* Available bandwidth

The project also provides tools for searching, modifying, adding, and displaying campus network connections.

---

## Main Objectives

* Represent campus locations as graph nodes.
* Represent cable connections as graph edges.
* Store cable length and cost.
* Track network capacity and current load.
* Calculate available bandwidth.
* Search connections by building/node name.
* Modify existing cable information.
* Add new cable connections.
* Add new campus buildings/nodes.
* Display all campus nodes.
* Display all cable connections.
* Provide a structured network-management system.

---

## Campus Nodes

The project contains campus locations including:

* Engineering Building
* YKSG-2
* RASG-1
* Food Court
* Auditorium
* AB-4
* Annex Building
* Admission Building
* Hall Accommodation
* ID Card Section
* Gate-4
* Gate-3
* Gate-2
* AB-1
* Teachers Home
* Gate-8
* Mosque
* AB-3
* Green Garden
* Gate-1
* Transport Building

These locations are stored in a `vector<string>` and accessed through node IDs.

---

## Graph Representation

Each network connection is represented using an `Edge` structure.

```cpp
struct Edge
{
    int u, v;
    int length;
    int cost;
    int capacity;
    int currentLoad;
};
```

Where:

* `u` = starting node
* `v` = destination node
* `length` = cable length in meters
* `cost` = cable/connection cost
* `capacity` = maximum bandwidth in Mbps
* `currentLoad` = currently used bandwidth in Mbps

The default network capacity is **100 Mbps**.

---

## Network Information Display

For every connection, the system can display:

```text
Connection
Length
Cost
Capacity
Current Load
Available Bandwidth
```

Available bandwidth is calculated as:

```text
Available Bandwidth = Capacity - Current Load
```

This allows the user to understand the current state of a particular network connection.

---

## Main Features

### 1. Show All Campus Nodes

The system can display every registered campus location along with its node ID.

---

### 2. Show All Connections

The system can display all existing cable connections and their:

* Length
* Cost
* Capacity
* Current Load
* Available Bandwidth

---

### 3. Search Connections

The user can enter a building/node name.

The system searches the network and finds every cable connection associated with that node.

---

### 4. Modify Connection

Existing connection information can be modified.

The user can change:

1. Cable Length
2. Cable Cost
3. Capacity
4. Current Load
5. All connection information

The system also checks whether the new current load exceeds the connection capacity.

---

### 5. Add New Connection

A new connection can be created between two existing campus nodes.

The user provides:

* First node
* Second node
* Cable length
* Cable cost
* Cable capacity
* Current load

The program validates the bandwidth information before adding the connection.

---

### 6. Add New Building / Node

The system can dynamically add a new campus location.

After adding the new node, the user can connect it with multiple existing nodes.

For every new connection, the system stores:

```text
Length
Cost
Capacity
Current Load
```

This makes the network structure expandable without rewriting the existing node list.

---

## Searching Algorithm

The project includes a **Binary Search** function for searching a connection based on its serial position.

The algorithm repeatedly divides the search range into two parts until the target is found or the search range becomes empty.

### Complexity

```text
Time Complexity: O(log n)
```

for the binary-search operation on the indexed sequence.

---

## Modify Data Panel

The central data-management panel provides:

```text
1. Search & Modify Connection
2. Add New Connection
3. Add New Building / Node
4. Show All Nodes
5. Show All Connections
6. Back to Main Panel
```

This works as the main administration section for managing the network data.

---

## Conceptual Graph Model

```text
Campus Building = Node

Cable Connection = Edge

Edge Information:
    ├── Length
    ├── Cost
    ├── Capacity
    └── Current Load
```

Example:

```text
Engineering Building
        |
      Cable
        |
     YKSG-2
```

The complete campus network is therefore represented as a graph.

---

## Programming Concepts Used

* C++
* Structures
* Vectors
* Strings
* Graph representation
* Edge and node modeling
* Searching
* Binary Search
* Loops
* Conditional statements
* Functions
* Dynamic data modification
* Input validation
* Menu-driven programming

---

## Data Structure

The primary graph data is stored using:

```cpp
vector<string> nodeName;
vector<Edge> edges;
```

This provides a simple representation of campus nodes and their connections.

---

## Technologies

**Language:** C++

**Application Type:** Console-based Network Management System

**Core Concepts:** Graph, Nodes, Edges, Vector, Searching, Binary Search

---

## Learning Outcomes

This project provided practical experience with:

* Graph-based problem modeling.
* Representing real-world infrastructure using nodes and edges.
* Managing structured network data.
* Searching and modifying graph-related information.
* Working with vectors and structures.
* Implementing dynamic addition of nodes and edges.
* Applying validation rules to network capacity and load.

---

## Project Type

**Academic C++ / Data Structures & Graph-Based Project**

The project demonstrates how graph concepts can be applied to a practical campus cable/network management problem.
