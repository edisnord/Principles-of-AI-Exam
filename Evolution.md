### What is the general control strategy of evolutionary algorithms?

They use an irrevocable strategy.

### What does the evolutionary algorithm store in its global workspace?

It stores a population of individuals which change over time, the fitness function
and it's operators (selection, recombination, mutation, replacement).

### Which of these is NOT an evolutionary operator?

The evolutionary operators are:
- selection
- recombination
- mutation
- replacement

### How do we code an individual?

An individual can be represented in many ways. The code behind an individual is called a Gene, and this gene should be dismembered property by property to allow for their change.

### How many steps does the evolutionary cycle consist of?

It consists of 4 steps:
- **Selection**: The selection of individuals from a population based on a selection rule
- **Recombination**: The construction of offspring from the selected individuals based on some recombination strategy
  - Repair might be necessary if some invariants are violated from recombination
- **Mutation**: The random modification of the generated offspring in order to stochastically create new members for our population (should not violate invariants)
- **Replacement**: In replacement you swap out individuals of the old population with the offspring that were created from the cycle based off an offspring rate and replacement rate.
    - if offspring rate > replacement rate, you must perform selection again to remove some offspring
    - If replacement rate > offspring rate, you must perform selection again to select some offspring to use multiple times in the population
    - If they are equal, then you just do a total exchange.

### Where can we incorporate randomness into the evolutionary algorithm?

Randomness can be incorporated in every step of the evolutionary algorithm, from selection to replacement. Selection can possibly not be random if you use Culling.

### Where do we use selection in the evolutionary algorithm?

You use selection in the selection step, and possibly in replacement based on what rates of offspring and replacement you have chosen.

### What is a good selection algorithm in evolutionary algorithms?

Good ones are the ones that allow you to also select one of the worse members of a population once in a while, because that can help you get out of periods of stagnation. Some of these algorithms are:
- Roulette selection
- Tournament selection
- Ranking 

### What is the connection between crossover and recombination?

Crossover is a recombination algorithm.

### When does the evolutionary algorithm terminate?

When a goal individual has appeared in our population

### Which of these is not a strategy parameter of evolutionary algorithms?

Some strategy parameters are: 
- size of the population
- probability of mutation
- rate of the offspring
- rate of the replacement
