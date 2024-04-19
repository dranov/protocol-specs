# Paxos

[Paxos](https://en.wikipedia.org/wiki/Paxos_(computer_science)) is a family of
protocols for solving consensus in a network of unreliable or fallible
processors.

This folder contains only specifications of single-decree Paxos.

Original sources of these specifications:

- [`Paxos.tla`](https://github.com/tlaplus/DrTLAPlus/blob/b74cff5f3616c7a4beb5416203c292e818e87b5a/Paxos/Paxos.tla) – from the inaugural Dr. TLA+ lecture

- `paxos_fol.ivy` and `paxos_epr.ivy`, from the
  [artifact](https://cs.stanford.edu/~padon/paxos-made-epr.html) associated with
  the [Paxos Made EPR](https://doi.org/10.1145/3140568) paper
  ([extended version](https://arxiv.org/abs/1710.07191))
    - `paxos_fol.ivy` has verification conditions in first order logic (FOL), and might require restrictions on the sizes of the domain for SMT solvers to terminate (see the last two lines in the file)
    - `paxos_epr.ivy` has VCs in a decidable fragment of FOL, following the transformation described in the Paxos Made EPR paper based on the `paxos_fol.ivy` specification

-
  [`paxos_fol.pyv`](https://github.com/wilcoxjay/mypyvy/blob/3a055dfad3d13fb35b6125ab6f43fa6ea4493b5f/examples/paxos_fol.pyv)
  and [`paxos_epr.ivy`](https://github.com/wilcoxjay/mypyvy/blob/3a055dfad3d13fb35b6125ab6f43fa6ea4493b5f/examples/paxos_epr.pyv) are translations of the above into mypyvy

