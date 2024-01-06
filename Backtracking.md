### What does the global workspace of backtracking search contain?

It contains one path from the start node to the current node with all untested outgoing arcs from the nodes of this path.

### What are the search rules of backtracking search?

- **append** a new untested outgoing arc driving from the current node to the end of the current path
- **remove** the last arc of the current path (backtrack)

### What is the control strategy of backtracking search?

applying the backtracking in the following cases:
- dead ends
- checked crossroads
- cycle (the current node can be found in the rest of the current path)
- depth bound (depth bound exceeded)

Some additional techniques can be added to the control strategy as well based on the problem:
- **ordinal strategy** : that ranks the outgoing arcs of the current node, and tries them to apply in order of their preference 
- **cutting strategy** : that ignores some untested outgoing arcs of the current node

### Which of these is NOT true about the first version of the backtracking search (BT1)?

BT1 is a simple version of a backtracking search algorithm, which only backtracks when dead ends are found and when all the crossroads of a node have been checked. It will always find the solution in a finite directed acyclic graph.

### Which of these statements is NOT true about the second version of the backtracking search (BT2)?

BT2 is a more complex version of BT1, which implements all the backtracking checks mentioned 2 questions ago. BT2 will always terminate in a delta-graph, and will find a solution if a solution path is within the depth bound.

### Which of these is an advantage of backtracking search?

Advantages of backtracking search:
- Always terminates and finds a solution (within the depth bound)
- implementation is simple
- small memory usage

Disadvantages:
- Doesn't find an optimal solution
- A wrong choice in the beginning might take lots of steps to be undone
- The same part of a graph can be traversed many times
