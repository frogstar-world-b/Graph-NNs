# Graph-NNs
Practical tutorials of PyTorch Geometric (aka PyG) are covered in this repo. Specifically, examples of increasing GNN architecture complexity are provided, and it is recommended that you complete them in the following order:

1. **intro**
   - `README.md`: Covers creating the **conda environment** needed to run the notebooks in this repo
   - `Karate_Club_Node_GCN_Classifier.ipynb`: A simple neural message passing scheme is utilized for classification using the graph convolutional operator `GCNConv`.
   - Dataset: [Zachary's karate club](https://pytorch-geometric.readthedocs.io/en/latest/generated/torch_geometric.datasets.KarateClub.html#torch_geometric.datasets.KarateClub) is a social network of a university karate club, described in the paper "An Information Flow Model for Conflict and Fission in Small Groups" by Wayne W. Zachary.
3. **node_classification**
    - `Node_Classification_with_MLP.ipynb`: A Multi-layer Perceptron Network (MLP) is used for classifying nodes in a single graph, where only node features are utilized. 
    - `Node_Classification_with_GNN.ipynb`: Two different GNN models (graph convolutional operator `GCNConv` and graph attentional operator `GATConv`) are utilized. Here, the graph structure is explicitly used, and unsurprisingly significant improvement in performance is observed.
    - Dataset: The [Cora](https://paperswithcode.com/dataset/cora#:~:text=The%20Cora%20dataset%20consists%20of,corresponding%20word%20from%20the%20dictionary.) dataset consists of scientific papers, where nodes represent documents, and edges represent citation relationships. Each paper is categorized into one of several research fields.
5. **graph_classification**
    - `Graph_Classification.ipynb`: Given a dataset of graphs, we want to classify each (entire) graph based on its structural inforation and additional features.
    - A new PyG operator, `GraphConv` is introduced to demonstrate the impact of including/omiting normalization. Plus, the addition of a skip-connection layer is explored.
    - Dataset: [MUTAG](https://paperswithcode.com/dataset/mutag) dataset represents chemical compounds, specifically mutagenic and non-mutagenic molecules. The graphs in the dataset describe the structure of these chemical compounds, with nodes representing atoms and edges representing chemical bonds.
  
Visualizing the embeddings is utilized in all notebooks to assess how well the GNN representation resembles the community-structure of the graph(s).  
