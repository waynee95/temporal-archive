# Temporal Logics

Büchi and Rabin showed that Monadic Second Order Logic (MSO) over infinite 
words or trees is decidable.

Temporal logics are fragments of MSO over words or trees. 

## Automata

The emptiness and membership problems of automata are used to decide _satisfiability_
and _model checking_ for various logics.

The type of automaton used (structures they operate on, rank of determinism,
acceptance condition) depends on the logic. 

Linear-time logics need automata over words, whereas branching-time logics
need automata over trees.
