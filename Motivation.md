# Why Quantum Computing?

---

## Chemistry

- Drugs/Materials/Fuels[^a] ![](<Attachments/Pasted image 20221214124223.png>)
- Experiments are expensive and slow, computer simulation is critical
- Theoretically, we know what to do:
  $$\hat{H}\ket{\psi} = i\hbar \tfrac{d}{dt} \ket{\psi}$$
- Exponential scaling, even small molecules would require earth sized hardware!

[^a]: [source](https://doi.org/10.1021/acs.oprd.0c00222 "DOI URL")

---

## Biology

- Protein folding
	- https://www.nature.com/articles/nrd1549
- Vaccination:
	- https://journals.aps.org/prl/abstract/10.1103/PhysRevLett.101.058701
	- use graph partitioning to minimize the number of vaccine doses needed to immunize a population (or network of computers)

---

## Computer Science

- Traveling salesman problem
	- Given a list of cities and the distances between each pair of cities, what is the shortest possible route that visits each city exactly once and returns to the origin city?
	- `NP-hard` 
	- It is used as a [benchmark](https://en.wikipedia.org/wiki/Benchmark_(computing) "Benchmark (computing)") for many optimization methods. Even though the problem is computationally difficult, many [heuristics](https://en.wikipedia.org/wiki/Heuristic "Heuristic") and [exact algorithms](https://en.wikipedia.org/wiki/Exact_algorithm "Exact algorithm") are known, so that some instances with tens of thousands of cities can be solved completely and even problems with millions of cities can be approximated within a small fraction of 1%.[[1]](https://en.wikipedia.org/wiki/Travelling_salesman_problem#cite_note-1)

- `Max-Cut` Problem
	- `NP-complete`
	- For a [graph](https://en.wikipedia.org/wiki/Graph_(discrete_mathematics) "Graph (discrete mathematics)"), a **maximum cut** is a [cut](https://en.wikipedia.org/wiki/Cut_(graph_theory) "Cut (graph theory)") whose size is at least the size of any other cut. That is, it is a [partition](https://en.wikipedia.org/wiki/Graph_partition "Graph partition") of the graph's [vertices](https://en.wikipedia.org/wiki/Vertex_(graph_theory) "Vertex (graph theory)") into two [complementary sets](https://en.wikipedia.org/wiki/Complement_(set_theory) "Complement (set theory)") S and T, such that the number of edges between S and T is as large as possible. Finding such a cut is known as the **max-cut problem**.
	- One wants a [subset](https://en.wikipedia.org/wiki/Subset "Subset") S of the vertex set such that the number of edges between S and the complementary subset is as large as possible. Equivalently, one wants a [bipartite](https://en.wikipedia.org/wiki/Bipartite_graph "Bipartite graph") subgraph of the graph with as many edges as possible.

- Circuit design
	- https://pubsonline.informs.org/doi/10.1287/opre.36.3.493