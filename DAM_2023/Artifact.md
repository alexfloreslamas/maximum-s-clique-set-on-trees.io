<script type="text/javascript" charset="utf-8" 
src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?config=TeX-AMS-MML_HTMLorMML,
https://vincenttam.github.io/javascripts/MathJaxLocal.js"></script>

# **Artifact page:** 'A dynamic programming algorithm for a maximum $s$-clique set on trees'

- [Home Page](../index.md)
- [Database Page](Database.md)
- [Reproducibility of results](Experiments.md)


**Authors:** [José Alberto Fernández-Zepeda](https://dblp.org/pid/13/7045), [Alejandro Flores-Lamas](https://alexfloreslamas.wixsite.com/alexfl), [Matthew Hague](https://www.cs.rhul.ac.uk/home/uxac009/), [Joel Antonio Trejo-Sánchez](https://www.cimat.mx/~joel.trejo).

---


## Description

Experiments in the article "A dynamic programming algorithm for a maximum $s$-clique set on trees" were done using the code in this page. This artifact contrains source code (in Python) for the implementations of the Schäfer’s[^1] and Max-D*s*T[^2] algorithms.


## Assets

**Artifact** The tool we used for the experiments for the paper submitted to [Discrete Applied Mathematics](https://www.sciencedirect.com/journal/discrete-applied-mathematics)

- [Download](./DAM_2023_Tool/DAM_2023_Tool.zip)

**Reproducibility of results**

- Please see this [web page](./Database.md) for information related to the database.

- Instructions to reproduce the experiments: [experimental web page](Experiments.md).


## Instructions

### General Installation

- There's no installation procedure; please download the project.

#### Software Dependencies

- DAM_2023_Tool is written in Python 3.10, yet it can be run on version 3.9x or later.

- DAM_2023_Tool also requires the following packages:
  - [NetworkX](https://networkx.org/)
  - [YAML](https://yaml.org/)
  - [pandas](https://pandas.pydata.org/)


#### Selected contents

See [Script files and folder structure](#script-files-and-folder-structure) for the entire contents of the artifact.

*Main file:*

- `/DAM_2023_Tool/main.py`

*Schäfer's implementation:*

- `/DAM_2023_Tool/src/Algorithms/DAM_2023/Schafer`

*Max-DsT implementation:*

- `/DAM_2023_Tool/src/Algorithms/DAM_2023/Max_DsT`

*I / O folders:*

- Input: `/DAM_2023_Tool/Input/`
- Output: `/DAM_2023_Tool/Output/`

*Configuration file:*

 * `/DAM_2023_Tool/Settings`
    * `DAM_2023_small_example.yaml` <-- Configuration file to execute Schäfer's and Max-D*s*T on three 'small-size' trees stored the path: `/DAM_2023_Tool/Input/Small`; result files will be stored in `/DAM_2023_Tool/Output/Small`.

    * `DAM_2023_medium_example.yaml` <-- Configuration file to execute both Schäfer's and Max-D*s*T on one 'medium-size' tree stored the path: `/DAM_2023_Tool/Input/Medium`; result files will be stored in `/DAM_2023_Tool/Output/Medium`.


### Other instructions and example of execution

After unpacking the artifact, DAM_2023_Tool can be run as follows:

- Open a command-line interpreter and navigate to the 'DAM_2023_Tool' folder.
- Type the following command: 

```bash
$ python main.py Settings/DAM_2023_small_example.yaml
```

In the above example, we call the `main.py` file with the parameters of `DAM_2023_small_example.yaml`. In particular this example proceeds as follows:


1. DAM_2023_Tool reads the GML files in `/DAM_2023_Tool/Input/Small`.
2. DAM_2023_Tool transforms each file into a tree with the attributes required by the algorithms.
3. DAM_2023_Tool executes Max-D*s*T and Schäfer's algorithms sequentially with the parameters specified in the YAML file.
4. DAM_2023_Tool saves in TSV files (`DAM_2023_Tool/Output/Small`) the outcome of the execution of the algorithms.

### Experimental Installation

- Instructions for repeating the experiments are provided on the [experimental web page](Experiments.md).


## Script files and folder structure

```
|-- DAM_2023_Tool
    |-- main.py
    |-- Input
    |   |-- Medium
    |   |   |-- random_30_000.gml
    |   |-- Small
    |       |-- input_graph_0.gml
    |       |-- input_graph_1.gml
    |       |-- input_graph_2.gml
    |-- Output
    |   |-- Medium
    |   |-- Small
    |   |-- T_22_16
    |   |-- T_B
    |   |-- T_D
    |   |-- T_L
    |   |-- T_Ph
    |   |-- T_eta
    |-- Settings
    |   |-- DAM_2023_medium_example.yaml
    |   |-- DAM_2023_small_example.yaml
    |   |-- T_22_16.yaml
    |   |-- T_B.yaml
    |   |-- T_D.yaml
    |   |-- T_L.yaml
    |   |-- T_Ph.yaml
    |   |-- T_eta.yaml
    |-- Tests
    |   |-- Testers
    |   |   |-- abstract_benchmark_tester.py
    |   |   |-- tree_k_clique_s_club_tester.py
    |   |-- Testing
    |       |-- run_Schafers_and_Max_DsT.py
    |-- src
        |-- Algorithms
        |   |-- DAM_2023
        |   |   |-- Max_DsT
        |   |   |   |-- downward_sweep.py
        |   |   |   |-- dp_msc_t_updated.py
        |   |   |   |-- upward_sweep_updated.py
        |   |   |-- Schafer
        |   |       |-- my_tree_s_club.py
        |   |       |-- tree_s_club_updated.py
        |   |-- Enums
        |       |-- enum_algorithms.py
        |-- Graphs
        |   |-- Enums
        |   |   |-- enum_node_type.py
        |   |-- Graph
        |   |   |-- directed_tree.py
        |   |   |-- simple_directed_tree.py
        |   |   |-- simple_graph.py
        |   |   |-- simple_undirected_tree.py
        |   |-- Nodes
        |       |-- simple_node.py
        |       |-- TreeNodes
        |           |-- directed_tree_node.py
        |           |-- dkclique_node.py
        |           |-- schafers_node.py
        |           |-- simple_directed_tree_node.py
        |           |-- simple_undirected_tree_node.py
        |-- Utils
            |-- input_handler.py
            |-- output_handler.py
            |-- utils.py
```

---

## License

- Free

---


[^1]: Schäfer, A.: Exact algorithms for *s*-club finding and related problems. Ph.D. thesis, Friedrich-Schiller-University Jena (2009).
[^2]: Our dynamic programming algorithm that finds a maximum *s*-clique on trees.

[//]: # Style for tables and paragraph

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
