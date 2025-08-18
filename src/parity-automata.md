# Parity Automata

Parity automata are best suited for fixpoint logics with (fixpoint) alternation.

In a parity automata each _state_ is assigned a _priority_, and _acceptance_
means the _parity_ of the least priority seen _infinitely_ often in a run must
be even.

Least and greatest fixpoints are recursion mechanisms that are translated 
into automata states. 

- A least fixpoint quantifier can be understood as a recursive program that 
terminates eventually, and
- A greatest fixpoint quantifier can be understood as a recursive program that
runs infinitely.

Then we can say that states constructed from least fixpoint quantifiers get 
assigned an _odd_ priority, and those constructed from greatest fixpoint
quantifiers get assigned _even_ priorities.

## Logics

- Parity tree automata \\(\longleftrightarrow\\) modal \\(\mu\\)-calculus
- Parity word automta \\(\longleftrightarrow\\) linear time \\(\mu\\)-calculus \\(\mu TL\\)
