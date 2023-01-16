**Constraint Satisfaction Problems** are a generic family of classical optimization problems where one wants to find some optimal choice of variables which satisfies a given number of constraints on those variables. 

[Here](https://cis.temple.edu/~giorgio/cis587/readings/constraints.html) is a list of a few CSP examples.


## Max-Cut
In `Max-Cut` we try to partition the nodes of a graph into two groups while maximizing the number of edges cut (or connecting the two groups).

- [6-Node example](<./6-Node Max-Cut.md>)

- Nice example from Qiskit: https://qiskit.org/documentation/optimization/tutorials/06_examples_max_cut_and_tsp.html


- https://arxiv.org/abs/1909.08846v1
	- Quote: 
	  > Focal points of study in approximation algorithms are Boolean constraint satisfaction problems (CSPs) such as Max-SAT and Max-Cut, in which one is roughly given a set of local constraints acting on k ∈ O(1) bits each (out of a total of n bits), and asked to compute the largest number of constraints which are simultaneously satisfiable.
	- describes the mapping of optimization problems to Hamiltonian ground states


- [max-cut video](https://www.youtube.com/watch?v=mD-0VpNSJA0) This video demonstrates how physical systems that emulate an ising model can find the ground state. In this example, a set of coupled metronomes is used. 

- Connection between Ising model and Max-cut: https://arxiv.org/pdf/1501.07030.pdf