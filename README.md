# Graph-NNs

Graphs are a ubiquitous data structures and a universal language for describing complex systems, such as social networks, interactions between atoms, and interactions between drugs and proteins.

In this repo, practical tutorials of PyTorch Geometric (aka PyG) are covered. These tutorials are adapted from [PyTorch Geometric](https://pytorch-geometric.readthedocs.io/en/latest/get_started/colabs.html) examples, and expanded to include additional explorations. 

Specifically, this repo includes examples of increasing GNN architecture complexity, and it is recommended that you complete them in the following order:

1. **intro**
   - `README.md`: Covers creating the **conda environment** needed to run the notebooks in this repo
   - `Karate_Club_Node_GCN_Classifier.ipynb`: A simple neural message passing scheme is utilized for classification using the graph convolutional operator `GCNConv`.
   - Dataset: [Zachary's karate club](https://pytorch-geometric.readthedocs.io/en/latest/generated/torch_geometric.datasets.KarateClub.html#torch_geometric.datasets.KarateClub) is a social network of a university karate club, described in the paper "An Information Flow Model for Conflict and Fission in Small Groups" by Wayne W. Zachary.
3. **node_classification**
    - `Node_Classification_with_MLP.ipynb`: A Multi-layer Perceptron Network (MLP) is used for classifying nodes in a single graph, where only node features are utilized. 
    - `Node_Classification_with_GNN.ipynb`: Two different GNN models (graph convolutional operator `GCNConv` and graph attentional operator `GATConv`) are utilized. Here, the graph structure is explicitly used, and unsurprisingly significant improvement in performance is observed.
    - Dataset: The [Cora](https://paperswithcode.com/dataset/cora#:~:text=The%20Cora%20dataset%20consists%20of,corresponding%20word%20from%20the%20dictionary.) dataset consists of scientific papers, where nodes represent documents, and edges represent citation relationships. Each paper is categorized into one of several research fields.
5. **graph_classification**
    - `Graph_Classification.ipynb`: Given a dataset of graphs, the goal is to classify each (entire) graph based on its structural information and additional features.
    - A new PyG operator, `GraphConv` is introduced to demonstrate the impact of including/omitting neighborhoold information normalization. Plus, the addition of a skip-connection layer is explored.
    - Dataset: [MUTAG](https://paperswithcode.com/dataset/mutag) dataset represents chemical compounds, specifically mutagenic and non-mutagenic molecules. The graphs in the dataset describe the structure of these chemical compounds, with nodes representing atoms and edges representing chemical bonds.
  
Visualizing embeddings is utilized in all notebooks to assess how well the GNN representation resembles the community-structure of the graph(s).

Finally, reading the first five chapters of [Graph Representation Learning by William L. Hamilton](https://www.cs.mcgill.ca/~wlh/grl_book/) is highly recommended to get comfortable with graph theory and graph neural networks lingo before you dive into code. The book provides intution, mathematical proofs, and explanations important to understanding why GNNs work, and and why/how different architectures impact model performance.


## References:
- [PyTorch Geometric](https://pytorch-geometric.readthedocs.io/en/latest/get_started/colabs.html)
- [Graph Representation Learning by William L. Hamilton](https://www.cs.mcgill.ca/~wlh/grl_book/)
