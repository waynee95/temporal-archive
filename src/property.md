# Properties

A _set of traces_ \\(P \subseteq \Sigma^\omega\\) is called a _trace property_
(or linear-time property).

A trace property can be checked one trace at a time.

A trace property \\(P\\) is a _safety property_ if it holds that for every trace
\\(t \not\in P\\): there exists a \\(u \sqsubseteq t\\) such that for every 
\\(t'\\) with \\(u \sqsubseteq t'\\), we have \\(t' \not\in P\\).

A trace property \\(P\\) is a _liveness property_ if for every \\(u \in \Sigma^*\\):
there exists a \\(t \in \Sigma^\omega\\) with \\(ut \in P\\).
