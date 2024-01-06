- [What does the global workspace of graph search contain?](#what-does-the-global-workspace-of-graph-search-contain)
- [What is the search rule of graph search?](#what-is-the-search-rule-of-graph-search)
- [What is the control strategy of graph search?](#what-is-the-control-strategy-of-graph-search)
- [What kind of nodes are the open nodes?](#what-kind-of-nodes-are-the-open-nodes)
- [How do we call the subgraph we store in the global workspace of graph search?](#how-do-we-call-the-subgraph-we-store-in-the-global-workspace-of-graph-search)
- [What kind of nodes are the closed nodes?](#what-kind-of-nodes-are-the-closed-nodes)
- [What does the parent pointer function (pi) point to?](#what-does-the-parent-pointer-function-pi-point-to)
- [When is an evaluation function decreasing?](#when-is-an-evaluation-function-decreasing)
- [When is a node of a search graph correct?](#when-is-a-node-of-a-search-graph-correct)
- [Which of these statements is true about the general graph search?](#which-of-these-statements-is-true-about-the-general-graph-search)
- [Can we use order heuristic as a secondary control strategy in an uninformed graph search?](#can-we-use-order-heuristic-as-a-secondary-control-strategy-in-an-uninformed-graph-search)
- [Which of these is depth first search (f is the evaluation function, g is the cost function, c is the cost of an edge)?](#which-of-these-is-depth-first-search-f-is-the-evaluation-function-g-is-the-cost-function-c-is-the-cost-of-an-edge)
- [Which of these is breadth first search (f is the evaluation function, g is the cost function, c is the cost of an edge)?](#which-of-these-is-breadth-first-search-f-is-the-evaluation-function-g-is-the-cost-function-c-is-the-cost-of-an-edge)
- [Which of these is uniform cost search (f is the evaluation function, g is the cost function, c is the cost of an edge)?](#which-of-these-is-uniform-cost-search-f-is-the-evaluation-function-g-is-the-cost-function-c-is-the-cost-of-an-edge)
- [What does admissibility mean for a graph search?](#what-does-admissibility-mean-for-a-graph-search)
- [Which statement is NOT true about the constant 0 function?](#which-statement-is-not-true-about-the-constant-0-function)
- [Which of these is the look-forward graph search (f is the evaluation function, g is the cost function, h is the heuristic, h-star is the optimal cost, c is the cost of an edge)?](#which-of-these-is-the-look-forward-graph-search-f-is-the-evaluation-function-g-is-the-cost-function-h-is-the-heuristic-h-star-is-the-optimal-cost-c-is-the-cost-of-an-edge)
- [Which of these is the A algorithm (f is the evaluation function, g is the cost function, h is the heuristic, h-star is the optimal cost, c is the cost of an edge)?](#which-of-these-is-the-a-algorithm-f-is-the-evaluation-function-g-is-the-cost-function-h-is-the-heuristic-h-star-is-the-optimal-cost-c-is-the-cost-of-an-edge)
- [Which of these is the A-star algorithm (f is the evaluation function, g is the cost function, h is the heuristic, h-star is the optimal cost, c is the cost of an edge)?](#which-of-these-is-the-a-star-algorithm-f-is-the-evaluation-function-g-is-the-cost-function-h-is-the-heuristic-h-star-is-the-optimal-cost-c-is-the-cost-of-an-edge)
- [Which of these is the A-c (consistent) algorithm (f is the evaluation function, g is the cost function, h is the heuristic, h-star is the optimal cost, c is the cost of an edge)?](#which-of-these-is-the-a-c-consistent-algorithm-f-is-the-evaluation-function-g-is-the-cost-function-h-is-the-heuristic-h-star-is-the-optimal-cost-c-is-the-cost-of-an-edge)
- [Which of these is a property of the A algorithm?](#which-of-these-is-a-property-of-the-a-algorithm)
- [Which of these is not true for A-c algorithm](#which-of-these-is-not-true-for-a-c-algorithm)
- [When do we say that a heuristic function is monotone?](#when-do-we-say-that-a-heuristic-function-is-monotone)
- [Which of these statements is NOT true about breadth-first search?](#which-of-these-statements-is-not-true-about-breadth-first-search)
- [Which of these is true about uniform cost search?](#which-of-these-is-true-about-uniform-cost-search)


### What does the global workspace of graph search contain?

It contains:
- The search graph (the paths starting from the start node)
- The open nodes (frontier/nodes to be expanded)

### What is the search rule of graph search?

Expand open nodes until there are no more open nodes or a we found the goal node

### What is the control strategy of graph search?

selects an open node to be expanded based on an evaluation function

### What kind of nodes are the open nodes?

They are the neighbors of previous open nodes which will be expanded in the future steps of the graph search algorithm. They are either unexplored or in need of having their cost recalculated

### How do we call the subgraph we store in the global workspace of graph search?

It's called a search graph.

### What kind of nodes are the closed nodes?

These are nodes that have already been explored, have a parent associated with them and their cost is calculated.

### What does the parent pointer function (pi) point to?

Given a node, the parent pointer function will return the node which comes before the given node in the path from the start node to the goal one. So it returns the pointer to the parent of the node in the path. 

### When is an evaluation function decreasing?

An evaluation function is decreasing if for lower values of a path's cost, it returns lower values. So it should decrease with the cost.

### When is a node of a search graph correct?
The node m is correct if g(m) and pi(m) are consistent and optimal

$$
    g(m) = c^\pi(start, m) \\
    c^\pi(start, m) = \min_{\alpha \in \set{start \longrightarrow m} \cap G
    } c^\alpha(start, m)
$$


### Which of these statements is true about the general graph search?

General graph search is a graph search algorithm whose global workspace contains:
- The search graph $G$
- The set of open nodes $OPEN$
- The evaluation function $f:OPEN \rightarrow \R$
- The parent-pointer function $\pi: \text{Node} \rightarrow \text{Node}$
- The cost function $g: \text{Node} \rightarrow \R$

This algorithm searches for a goal node, and while searching it builds a graph $G$ with the nodes it has found, and updates the cost function to reflect the optimal path from the start node to the end one. It also maintains the correctness of its nodes by putting the children of a node whose parent has changed into the set of open nodes for expansion.

It can be proven that:
- Each node is expanded only finite times in a $\delta$-graph.
- The general graph-search always terminates in a
finite $\delta$-graph.
- The general graph-search finds a solution in a finite $\delta$-graph if there exists a solution.

### Can we use order heuristic as a secondary control strategy in an uninformed graph search?

Yes, we can

### Which of these is depth first search (f is the evaluation function, g is the cost function, c is the cost of an edge)?

$$
    f = -g\\
    c(n,m) = 1, \hspace{0.2cm} \forall n,m \in N
$$

### Which of these is breadth first search (f is the evaluation function, g is the cost function, c is the cost of an edge)?

$$
    f = g\\
    c(n,m) = 1, \hspace{0.2cm} \forall (n,m) \in N
$$

### Which of these is uniform cost search (f is the evaluation function, g is the cost function, c is the cost of an edge)?

$$
f = g
$$

### What does admissibility mean for a graph search?

Admissibility of a heuristic function is a property that is defined as: $h(n) \leq h^*(n), \forall n \in N$, with $h^* = c^*(n, T)$. It means that a heuristic function is always less than or equal to the optimal cost from a node $n$ to the target $T$.

### Which statement is NOT true about the constant 0 function?

The constant 0 function is a heuristic function that is non-negative, admissable and monotone. It simply returns 0 in all cases.

### Which of these is the look-forward graph search (f is the evaluation function, g is the cost function, h is the heuristic, h-star is the optimal cost, c is the cost of an edge)?

$$
    f = h\\
$$

### Which of these is the A algorithm (f is the evaluation function, g is the cost function, h is the heuristic, h-star is the optimal cost, c is the cost of an edge)?

$$
    f = h \\
    h \ge 0\\
$$

### Which of these is the A-star algorithm (f is the evaluation function, g is the cost function, h is the heuristic, h-star is the optimal cost, c is the cost of an edge)?

$$
    f = h \\
    h \ge 0\\
    h \le h^*
$$

### Which of these is the A-c (consistent) algorithm (f is the evaluation function, g is the cost function, h is the heuristic, h-star is the optimal cost, c is the cost of an edge)?

$$
    f = h \\
    h \ge 0\\
    h \le h^*\\
    h(n) - h(m) \le c(n,m), \forall (n,m) \in G
$$

### Which of these is a property of the A algorithm?

The algorithm is an informed graph search algorithm, whose heuristics must have the non-negative value property. Its evaluation function is equal to the sum of the cost of a node from the start and the output of the heuristic function.


### Which of these is not true for A-c algorithm

The A-c (A-consistent) algorithm is an informed graph search algorithm which requires its heuristic functions to have the properties of being non-negative, being admissible and being monotone. Its evaluation function is equal to the sum of the cost of a node from the start and the output of the heuristic function.

### When do we say that a heuristic function is monotone?

A heuristic function is monotone when the difference between the heuristic values of two nodes $n$ and $m$ is always less than or equal to the cost from n to m. Put in math:

$$
h(n) - h(m) \le c(n,m)
$$

### Which of these statements is NOT true about breadth-first search?

Breadth-first search is an uninformed graph search algorithm which traverses nodes of the same depth, depth by depth. The cost of all the arcs in the graph are treated as if being 1, and the open nodes are selected based on the minimal cost.

### Which of these is true about uniform cost search?

Uniform cost search is an uninformed graph search algorithm whose evaluation function is just the positive cost of a node from the start point, and selects an open node based on the minimum evaluation function value.