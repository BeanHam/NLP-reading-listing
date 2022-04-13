## MRC with Graph Neural Network (GNN)

:+1: : relevant :question: : still need to understand

Graphs in question-answering domain are usually referred as knowledge graphs (KG). In our case, however, we do not work with knowledge-based QA. Instead, we work on MRC-QA, the dataset of which usually does not come with knowledge graphs. Therefore, we focus on the literature that automatically **generates** graphs.

---
- **(2018)** [Question Answering by Reasoning Across Documents with Graph Convolutional Networks](https://arxiv.org/abs/1808.09920) 
- **(2019)** [Cognitive Graph for Multi-Hop Reading Comprehension at Scale](https://arxiv.org/abs/1905.05460)
- :question: :+1: **(2019)** [BP-Transformer: Modelling Long-Range Context via Binary Partitioning](https://arxiv.org/abs/1911.04070)
  - binary partitioning of documents + construct graphs + attention 
- :+1: **(2019)** [Dynamically Fused Graph Network for Multi-hop Reasoning](https://aclanthology.org/P19-1617/)
  - paragraph selectors -> using corenlp toolkit to extract entities + construct entity graph -> query & context embedding -> match embedding with entity graph -> prediction
- :+1: **(2019)** [Multi-hop Reading Comprehension across Multiple Documents by Reasoning over Heterogeneous Graphs](https://aclanthology.org/P19-1260/)
  -  instead of constructing graph with single type of nodes, they used heterogeneous graphs (entity nodes, document nodes, candidate nodes)
- **(2020)** [Coarse and Fine Granularity Graph Reasoning for Interpretable Multi-Hop Question Answering](https://ieeexplore.ieee.org/document/9037288)
  - coarse level graph: sentence graph; fine graph: entity graph  
- :+1: **(2020)** [Select, Answer and Explain: Interpretable Multi-Hop Reading Comprehension over Multiple Documents](https://arxiv.org/abs/1911.00484)
- :+1::tada: **(2020)** [GraphFlow: Exploiting Conversation Flow with Graph Neural Networks for Conversational Machine Comprehension](https://arxiv.org/abs/1908.00059) 
  - construct the graphs at the word level
  - unlike previous works, in which the ground-truth graphs are available (KB-graphs) or are manually created (using entities), they used adjacency matrix among words as a semantic graph (**fantastic**), which automates the process.
