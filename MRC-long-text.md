## MRC with Long Text

:+1: : relevant; :question: : still need to understand

---
- **(2018)** [A Multi-Stage Memory Augmented Neural Network for Machine Reading Comprehension](https://aclanthology.org/W18-2603/) 
  - use memory controller (BiGRU); complicated... 
- :+1: **(2018)** [Efficient and Robust Question Answering from Minimal Context over Documents](https://arxiv.org/abs/1805.08092)
  - finding: most questions can be answered with a small set of sentences.
  - sentence selector: question & sentences embedding -> scores indicating if the sentences can be used to answer the questions (thresholding on the scores) -> QA model
- **(2018)** [Towards Reading Comprehension for Long Documents](https://www.ijcai.org/proceedings/2018/0638.pdf)
  - hierachical-LSTM: token/character-level embedding + query embedding -> attention -> paragraph label
  - complicated
- **(2019)** [A Hierarchical Attention Retrieval Model for Healthcare Question Answering](https://dl.acm.org/doi/abs/10.1145/3308558.3313699)
  - IR (not MRC)
  - Idea:word-level, sentence-level, and document attention; (after word-level attention -> aggregate to sentence level + attention -> aggregate to document level attention)
- :question: :+1: **(2019)** [BP-Transformer: Modelling Long-Range Context via Binary Partitioning](https://arxiv.org/abs/1911.04070)
  - binary partitioning of documents + construct graphs + attention 
- **(2019)** [Simple and Effective Curriculum Pointer-Generator Networks for Reading Comprehension over Long Narratives](https://aclanthology.org/P19-1486/)
- **(2019)** [Token-level Dynamic Self-Attention Network for Multi-Passage Reading Comprehension](https://aclanthology.org/P19-1218/)
  - multi-passages (we can think of the document as multi sentences/chunks)
- **(2020)** [CogLTX: Applying BERT to Long Texts](https://proceedings.neurips.cc/paper/2020/file/96671501524948bc3937b4b30d0e57b9-Paper.pdf)
  - split long documents into small blocks + retrieve relevant blocks and reform them into a document with L<=512 in order -> then go through BERT 
- :+1: **(2020)** [Question Answering with Long Multiple-Span Answers](https://aclanthology.org/2020.findings-emnlp.342/)
  - MASH-QA 
  - sentence selector: sentence+query attention -> sparse inter-sentence attention 
- :+1: **(2020)** [Recurrent Chunking Mechanisms for Long-Text Machine Reading Comprehension](https://arxiv.org/abs/2005.08056)
  - dynamic block chunking with reinforcement learning + binary prediction for blocks + answer extraction
- :+1: **(2021)** [RoR: Read-over-Read for Long Document Machine Reading Comprehension](https://arxiv.org/abs/2109.04780)
  - sliding window to generate blocks -> extract regional answer spans from each block -> compact regional answers as a new passage using MSC (minimum span coverage) -> extract another global answer span using this new passage -> rerank all answers
