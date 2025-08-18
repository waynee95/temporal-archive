# Linear-time \\(\mu\\)-calculus

Let \\(\Sigma = \\{a, b, \ldots \\}\\) be a finite alphabet, and let 
\\(\mathcal{V} = \\{X, Y, \ldots\\}\\) be a set of propositional variables.

## Syntax

Formulas of the linear-time \\(\mu\\)-calculus \\(\mu TL\\) are defined 
by the following grammar:

\\[
  \varphi ::= a \mid X \mid \varphi \lor \varphi \mid \varphi \land \varphi \mid 
    \bigcirc \varphi \mid \mu X. \\, \varphi \mid \nu X. \\, \varphi
\\]

where \\(a \in \Sigma\\) and \\(X \in \mathcal{V}\\).

## Semantics

We assume formulas to be well-named, i.e. a variable is not quantified more 
than once.

Formulas are interpreted over \\(\sigma\\)-words \\(w \in \Sigma^\omega\\).
A variable assignment (or environment) \\(\rho : \mathcal{V} \to 2^\mathbb{N}\\)
maps variables to sets of natural numbers. With \\(\rho[X \mapsto M]\\)
we denote the function that maps \\(X\\) to \\(M\\) and agrees with 
\\(\rho\\) on all other values.

Then the semantics of a formula is defined inductively as:

- \\([\\![ a ]\\!]^w_\rho := \\{i \in \mathbb{N} \mid w(i) = a\\} \\)
- \\([\\![ X ]\\!]^w_\rho := \rho(X) \\)
- \\([\\![ \varphi \lor \psi ]\\!]^w_\rho := \[\\![ \varphi ]\\!]^w_\rho \cup [\\![ \psi ]\\!]^w_\rho \\)
- \\([\\![ \varphi \land \psi ]\\!]^w_\rho := \[\\![ \varphi ]\\!]^w_\rho \cap [\\![ \psi ]\\!]^w_\rho \\)
- \\([\\![ \bigcirc \varphi ]\\!]^w_\rho := \\{ i \in \mathbb{N} \mid i + 1 \in [\\![ \varphi]\\!]^w_\rho \\}\\)
- \\([\\![ \mu X. \\, \varphi ]\\!]^w_\rho := \bigcap\\{ M \subseteq \mathbb{N} \mid [\\![ \varphi]\\!]^w_\rho \subseteq M \\} \\)
- \\([\\![ \nu X. \\, \varphi ]\\!]^w_\rho := \bigcup\\{ M \subseteq \mathbb{N} \mid M \subseteq [\\![ \varphi]\\!]^w_\rho \\} \\)

We write \\(w \models_\rho \varphi\\) iff \\(0 \in [\\![ \varphi ]\\!]^w_\rho\\).
If \\(\varphi\\) is closed, then we write \\(w \models \varphi\\).

## Example Encodings

- Eventually \\(p\\): \\[\mu X. \\, (p \lor \bigcirc X)\\]
- Always \\(p\\): \\[\nu X. \\, (p \land \bigcirc X)\\]
- Infinitely often \\(p\\): \\[\nu X. \mu Y. \\, (p \land \bigcirc X) \lor \bigcirc Y\\]
  - Inner \\(\mu Y\\) = "either we see \\(p\\) now and then return to \\(X\\), or 
    we postpone by going to the next \\(Y\\)
  - Outer \\(\nu X\\) enforces this cycle forever: after each occurance of \\(p\\),
    we must re-enter the obligation and see another \\(p\\)
