# 🎨 Graph Coloring Visualization and Compression

This project demonstrates the generation of random graphs, the application of graph coloring algorithms, visualization of the results, and saving the graph data in a compressed `.gz` format using Python. It uses the `networkx` library for graph operations and `matplotlib` for visualization.

---

## 📌 Features

- ✅ Generate random undirected graphs using the Erdős–Rényi model
- 🎨 Color graphs using a greedy algorithm (`largest_first` strategy)
- 🖼️ Visualize colored graphs using Matplotlib
- 📀 Save the graph and its coloring in a compressed `.gz` format

---

## 🛠️ Technologies Used

- [NetworkX](https://networkx.org/) - Graph generation and algorithms
- [Matplotlib](https://matplotlib.org/) - Visualization
- [NumPy](https://numpy.org/) - Math utility
- [Gzip](https://docs.python.org/3/library/gzip.html) - Compression
- [Pickle](https://docs.python.org/3/library/pickle.html) - Object serialization

---

## 🚀 Getting Started

### 🔧 Installation

Make sure you have Python 3.x installed. Then install the required libraries:

```bash
pip install networkx matplotlib numpy
```

### ▶️ Running the Code

This project is implemented in a Jupyter Notebook named `Generating_Random_Graph.ipynb`. Open the notebook and run the cells sequentially to:

1. Generate a random graph with `num_nodes` and `num_edges`
2. Apply a greedy coloring algorithm
3. Display the graph with nodes colored by their assigned color
4. Save the graph and its coloring to `graph_coloring_data.gz`

---

## 📁 File Overview

| File                          | Description                                                  |
|-------------------------------|--------------------------------------------------------------|
| `Generating_Random_Graph.ipynb` | Jupyter Notebook to generate, color, visualize, and save a graph |
| `graph_coloring_data.gz`      | Compressed file containing the graph object and coloring dict|
| `README.md`                   | You’re reading it!                                           |

---

## 🧠 Understanding Graph Coloring

Graph coloring is the assignment of labels (colors) to vertices of a graph so that no two adjacent vertices share the same color. It's used in:

- Scheduling problems
- Map coloring
- Register allocation in compilers
- Frequency assignment

This project uses the **greedy coloring algorithm** with the `largest_first` strategy, which colors the nodes in descending order of their degrees.

---

## 📊 Example Output

![Graph Coloring Example](https://via.placeholder.com/600x400.png?text=Graph+Coloring+Visualization)

*(Replace the above placeholder with your actual visualization screenshot.)*

---

## 📆 Output

After execution, a file named `graph_coloring_data.gz` will be created, containing:

```python
{
  'graph': <networkx.classes.graph.Graph>,
  'coloring': {0: 0, 1: 1, 2: 0, ...}
}
```

To load this file later:

```python
import gzip, pickle

with gzip.open('graph_coloring_data.gz', 'rb') as f:
    data = pickle.load(f)

G = data['graph']
coloring = data['coloring']
```

---

## 🤝 Contributing

Contributions, issues, and feature requests are welcome!

1. Fork the repository
2. Create your branch: `git checkout -b feature/your-feature`
3. Commit your changes: `git commit -m 'Add your message'`
4. Push to the branch: `git push origin feature/your-feature`
5. Open a pull request

---

## 📄 License

This project is licensed under the [MIT License](LICENSE).

---

## ⭐️ Show Your Support

If you found this project useful, please ⭐️ the repository to help others discover it!

