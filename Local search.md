### Which of these algorithms use an irrevocable control strategy?

An irrevocable control strategy is a control strategy which does not allow a search algorithm to undo an action. Some algorithms that use an irrevocable control strategy are:
- Local search
- Evolutionary algorithm
- Resolution
  
### Which of these algorithms use a tentative control strategy?

A tentative control strategy is a control strategy which allows an algorithm to undo an action. Some algorithms that use this control strategy are:
- Backtracking
- Graph search
- rule-based reasoning

### Which of these is a general control strategy

A general control strategy in a search algorithm might imply a broad or versatile approach that is not specialized for a particular problem or scenario. It could be a strategy that aims to work well across a variety of search spaces.

### Can we think of the hill climbing method as a special case of tabu search?

No, the case is that tabu search is a special case of hill climbing.

### In how many places does simulated annealing use randomness?

Twice, in the child selection process and in the moment of choosing a new current node.

### Which of these is a drawback of the tabu search?

It has 2 drawbacks in the slides.
- The tabu set size needs to be selected a posteriori
- It can rarely find the goal without strong heuristics, and even with strong heuristics it can get stuck after wrong decisions or get stuck in a dead end.

### Which of these is FALSE for local search algorithms?

General info on local search algorithms:

Local search algorithms are search algorithms which are not aware of the entire search space or the true layout of a graph, and try to find solutions around the area of an initial state. They can have skewed ideas of a state graph and do not guarantee the convergence to a global minimum, as they don't have enough information to do so.

### Which of these is NOT a drawback of the hill climbing algorithm?

Drawbacks of hill climbing:
- Can easily get stuck in cycles, local optima and equidistant surfaces because it has no way of recognizing them.
- Can rarely find the solution without a really good heuristic function.

### Which of these algorithms was NOT invented to avoid hill climbing getting stuck in a dead end?

Most of them :P. But Tabu search is one that was created FOR this purpose.