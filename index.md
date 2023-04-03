<script type="text/javascript" charset="utf-8" 
src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML,
https://vincenttam.github.io/javascripts/MathJaxLocal.js"></script>

# 'A dynamic programming algorithm for a maximum $s$-clique set on trees'

**Authors:** [José Alberto Fernández-Zepeda](https://dblp.org/pid/13/7045), [Alejandro Flores-Lamas](https://alexfloreslamas.wixsite.com/alexfl), [Matthew Hague](https://www.cs.rhul.ac.uk/home/uxac009/), [Joel Antonio Trejo-Sánchez](https://www.cimat.mx/~joel.trejo).

---

## Abstract

Finding cliques in an undirected graph $G = (V_G, E_G)$ is a fundamental problem in social network analysis. However, in some cases, the strict definition of a clique (a complete subgraph of $G$) can be too restrictive to model some social concepts. To address this issue, we study a relaxed version of the clique, known as the $s$-clique. An $s$-clique is a maximal subgraph of $G$ in which the distance in $G$ between any pair of vertices of the subgraph is less than or equal to some positive integer $s$ (where a clique is simply a $1$-clique). Finding the maximum $s$-clique in a graph is a computationally challenging problem, as it is NP-hard for any $s$ in arbitrary graphs. To overcome this challenge, we present a simple dynamic programming algorithm that efficiently solves the maximum $s$-clique problem on an $n$-vertex tree in $O(s \cdot n)$ time for $s \geq 2$. This algorithm outperforms existing algorithms in theory and practice. This approach is a stepping stone to finding a maximum $s$-clique in less restrictive graphs.

**Keywords:** Distance $s$-clique, Graph algorithms, Trees, Dynamic programming, $s$-club.

---

- A dynamic programming algorithm for a maximum $s$-clique set on trees: 
  - [Artifact page](./DAM_2023/Artifact.md)
  - [Database page](./DAM_2023/Database.md)
  - [Reproducibility of results](./DAM_2023/Experiments.md)
- [License](./license)
- [Discrete Applied Mathematics](https://www.sciencedirect.com/journal/discrete-applied-mathematics). The Journal of Combinatorial Algorithms, Informatics and Computational Sciences.

---

[//]: # Style  for tables and paragraph

<style>
  table {
  border-collapse: collapse;
}

td, th {
  border: 1px solid #999;
  padding: 0.5rem;
  text-align: center;
}

p {
  text-align: justify;
}
</style>

