- [Which of these was NOT true about the two-player games we have been examining in the course?](#which-of-these-was-not-true-about-the-two-player-games-we-have-been-examining-in-the-course)
- [What does the state of a two-player games represent?](#what-does-the-state-of-a-two-player-games-represent)
- [What is the winning strategy in a two-player game?](#what-is-the-winning-strategy-in-a-two-player-game)
- [When do we cut in the alpha-beta algorithm?](#when-do-we-cut-in-the-alpha-beta-algorithm)
- [What is the stationary test for minimax search?](#what-is-the-stationary-test-for-minimax-search)
- [Which of these statements is NOT true about the game tree? / What is the game tree?](#which-of-these-statements-is-not-true-about-the-game-tree--what-is-the-game-tree)
- [Which of these is a step in the minimax algorithm?](#which-of-these-is-a-step-in-the-minimax-algorithm)


### Which of these was NOT true about the two-player games we have been examining in the course?

The 2 player games we examine in this course are turn-taking, perfect-informed,
finite and deterministic, zero-sum games. This means that they are played in 2 turns,
both players can always see all the information about the state of the game (not like Yu-Gi-Oh, poker, Magic the Gathering, etc.), either the number of the possible steps in a current state or the length of the plays of the game are finite, the plays of the game do not depend on chance and the sum of the payoff values at the end of the game for both players is equal to 0.

### What does the state of a two-player games represent?

The state holds the configuration of the game and the next player.

### What is the winning strategy in a two-player game?

A winning strategy is a path of game moves which always guarantees the victory of a player regardless of what the other player does.

### When do we cut in the alpha-beta algorithm?

When we have $\alpha \ge \beta$ for a node and it's parent.

### What is the stationary test for minimax search?

The stationary test is a test which checks whether a move needs a depth bound increase or not based on a stationary value picked as a hyper-parameter. This can be done in the case of a drastic increase in points or a drastic decrease from one state to the other, to ensure that this strange move does not play in the favor of the enemy.

### Which of these statements is NOT true about the game tree? / What is the game tree?

The game tree is a tree of states, in which the levels alternate between the players of the game. The children of a node represent possible future moves that the player might make on their turn. Their complexity varies on the complexity of the game, and for chess, the game tree cannot be computed at all.

### Which of these is a step in the minimax algorithm?

I don't get this question. But the step in the minimax algorithm is chosen based on node with the highest/lowest evaluation function output based on whether the minimizing or maximizing player is playing.