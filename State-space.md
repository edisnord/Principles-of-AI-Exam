- [Which of these is NOT a search algorithm](#which-of-these-is-not-a-search-algorithm)
- [How can we NOT reduce the complexity of a search space?](#how-can-we-not-reduce-the-complexity-of-a-search-space)
- [What does the complexity of a representation graph NOT depend on?](#what-does-the-complexity-of-a-representation-graph-not-depend-on)
- [Which of these is NOT true of a state space graph](#which-of-these-is-not-true-of-a-state-space-graph)
- [In which of these problems is the problem space NOT the same as paths of the representation graph starting from the start node?](#in-which-of-these-problems-is-the-problem-space-not-the-same-as-paths-of-the-representation-graph-starting-from-the-start-node)
- [Which of these is NOT true of a delta-graph?](#which-of-these-is-not-true-of-a-delta-graph)


### Which of these is NOT a search algorithm

The search algorithms covered in this course:
- Local search
- Backtracking search
- Graph search
- Evolutionary algorithm
- Resolution
- Rule-based reasoning

### How can we NOT reduce the complexity of a search space?

How to reduce the complexity of a search space:
- Pruning
- Select the best model for the problem (best invariants, preconditions, operators)

### What does the complexity of a representation graph NOT depend on?

It depends on:
- How much the graph branches
- Number of nodes and arcs
- The number of cycles and their size

### Which of these is NOT true of a state space graph

A state-space graph is a directed graph consisting of nodes, each representing a distinct state, and edges, representing possible transitions or actions between states.

Key Components:
1. Nodes (Vertices): Nodes in a state-space graph represent different possible states of the system or problem under consideration. Each node encapsulates the relevant information characterizing a particular state.

2. Edges (Arcs): Edges in the graph depict the possible transitions or actions that can be taken to move from one state to another. These transitions often involve the application of specific operations, decisions, or events.

3. Cost function: Accepts 2 nodes (an edge) and returns the cost to traverse from the first node to the second one. 

### In which of these problems is the problem space NOT the same as paths of the representation graph starting from the start node?

Some problems that are this way are:
- The N-Queens problem (The problem space is only map layouts of placed queens, no path information is stored)
- The satisfiability problem (SAT) (Slide 36, lesson 2)

### Which of these is NOT true of a delta-graph?

A delta graph is just a graph which has a positive constant lower bound delta on the cost values of arcs and has a finite number of outgoing arcs on each node.