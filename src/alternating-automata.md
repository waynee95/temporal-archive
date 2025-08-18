# Alternating Automata

Alternating Automata feature _nondeterministic_ and _universal_ choices.

Are a good fit for translating temporal logics into automata because: 

- A temporal logic has conjuctions and disjunctions which can easily be 
translated into automata states. 
- Alternating automata are usually more 
_succinct_ then (non-)deterministic automata, resulting in more efficient
decision procedures.

## Weak Alternating Automata

Usually, weakness means that there are \\(\omega\\)-regular languages that 
are not accepted by a weak automata. 

However, every alternating automaton can be translated into a weak alternating automaton.
