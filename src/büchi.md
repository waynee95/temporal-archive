# Büchi Automata

A nondeterministic _Büchi automaton_ (NBA) \\(\mathcal{A}\\) is a 5-tuple 
\\(A = (Q, q_I, \Sigma, \delta, F)\\), where

- \\(Q\\) is a finite set of states,
- \\(q_I \in Q\\) is the initial state,
- \\(\Sigma\\) is the alphabet,
- \\(\delta \subseteq Q \times \Sigma \times Q\\) is the transition relation, and,
- \\(F \subseteq Q\\) is a set of _accepting states_.

If \\(\delta\\) is a (partial) _function_, the automaton is a _deterministic_
Büchi automaton (DBA).

A trace (or word) \\(t \in \Sigma^\omega\\) is accepted by \\(\mathcal{A}\\) if there
exists an infinite run \\(\rho \in Q^\omega\\) such that \\(\rho\\) visits
states in \\(F\\) infinitely often, \\(\rho(0) = q_I\\), and, for all 
\\(i\\), \\(\rho(i + 1) \in \delta(\rho(i), t(i))\\).

Let \\(Inf(\rho)\\) be the set of all states that occur infinitely often in \\(\rho\\).
Then a run is accepting if \\(Inf(\rho) \cap F \neq \emptyset\\), i.e. at least
some accepting state is visited infinitely often.

The language of a NBA \\(\mathcal{A}\\) is \\(L(\mathcal{A}) := \\{ w \in \Sigma^\omega \mid \text{there is an accepting run of } \mathcal{A} \text{ on } w\\}\\).

A langauge \\(L \subseteq \Sigma^\omega\\)is called _Büchi-recognizable/definable_ if there is an NBA such that \\(L = L(\mathcal{A})\\).

An example for a Büchi automaton accepting the language \\(L((a^*b)^\omega)\\):
the language of all words that contain infinitely many bs:
<?xml version="1.0" standalone="no"?>
<!DOCTYPE svg PUBLIC "-//W3C//DTD SVG 1.1//EN" "https://www.w3.org/Graphics/SVG/1.1/DTD/svg11.dtd">
<svg width="800" height="600" version="1.1" xmlns="http://www.w3.org/2000/svg">
	<ellipse stroke="black" stroke-width="1" fill="none" cx="118.5" cy="238.5" rx="30" ry="30"/>
	<text x="112.5" y="244.5" font-family="Times New Roman" font-size="20">0</text>
	<ellipse stroke="black" stroke-width="1" fill="none" cx="363.5" cy="238.5" rx="30" ry="30"/>
	<text x="357.5" y="244.5" font-family="Times New Roman" font-size="20">1</text>
	<ellipse stroke="black" stroke-width="1" fill="none" cx="363.5" cy="238.5" rx="24" ry="24"/>
	<path stroke="black" stroke-width="1" fill="none" d="M 105.275,211.703 A 22.5,22.5 0 1 1 131.725,211.703"/>
	<text x="101.5" y="162.5" font-family="Times New Roman" font-size="20">a, b</text>
	<polygon fill="black" stroke-width="1" points="131.725,211.703 140.473,208.17 132.382,202.292"/>
	<path stroke="black" stroke-width="1" fill="none" d="M 338.112,254.433 A 207.112,207.112 0 0 1 143.888,254.433"/>
	<polygon fill="black" stroke-width="1" points="338.112,254.433 328.701,253.768 333.39,262.601"/>
	<text x="234.5" y="299.5" font-family="Times New Roman" font-size="20">b</text>
	<path stroke="black" stroke-width="1" fill="none" d="M 145.052,224.58 A 235.714,235.714 0 0 1 336.948,224.58"/>
	<polygon fill="black" stroke-width="1" points="145.052,224.58 154.395,225.891 150.324,216.757"/>
	<text x="224.5" y="195.5" font-family="Times New Roman" font-size="20">a, b</text>
	<polygon stroke="black" stroke-width="1" points="43.5,238.5 88.5,238.5"/>
	<polygon fill="black" stroke-width="1" points="88.5,238.5 80.5,233.5 80.5,243.5"/>
</svg>
