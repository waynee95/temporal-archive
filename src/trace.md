# Traces

Let \\(\Sigma\\) be an alphabet.

An infinite sequence \\(t \in \Sigma^\omega\\) is called a _trace_, a 
finite sequence \\(t \in \Sigma^*\\) a _finite trace_.

For a trace \\(t\\) and a natural number \\(i \geq 0\\), we denote the \\(i\\)-th
element of the trace by \\(t(i)\\).

For a natural number \\(j \geq i\\), \\(t[i, j]\\) denotes the sequence
\\(t(i)t(i + 1) \ldots t(j - 1)t(j)\\).

For an infinite trace \\(t\\), \\(t[i, \infty]\\) denotes the infinite _suffix_
of \\(t\\), starting at position \\(i\\).

For two traces \\(t, t'\\) over \\(\Sigma\\) and \\(\Sigma'\\), we define 
the _zip_ operation \\(zip(t, t') = (t(0), t'(0)), (t(1)t'(1)) \ldots\\),
which defines a trace over \\(\Sigma \times \Sigma'\\).

We call \\(u \in \Sigma^\*\\) a _prefix_ of \\(t \in \Sigma^\omega \cup \Sigma^\*\\),
written \\(u \sqsubseteq t\\), if for some \\(n, |u| = n, |t| \geq n\\), and
\\(u[0, n] = t[0, n]\\).
