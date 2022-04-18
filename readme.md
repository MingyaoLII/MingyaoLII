# Environment

    Python                        3.9.7
    ogb                           1.3.3
    pandas                        1.4.1
    networkx                      2.6.3
    matplotlib                    3.5.1
    torch                         1.11.0
    torch-cluster                 1.6.0
    torch-geometric               2.0.4
    torch-scatter                 2.0.9
    torch-sparse                  0.6.13
    torch-spline-conv             1.2.1

# Datasets

[ogbn-arxiv](https://ogb.stanford.edu/docs/nodeprop/#ogbn-arxiv) Downloaded/Used in the directory `'./data'` by running the **Dataset** part in our code.

# Experiments

1. Make sure you satisfy the [environment](#Environment).

2. Run the `.ipynb` file to reproduce our experiment results.
   1. Run [Code Architecture-Implementation](#Code-Architecture) for initialization.
   2. Run [Code Architecture-Results](#Code-Architecture) for results reproduction.
   3. Every method is coded independently and all the outputs are attached. Arguments can be editted in `args={...}` in every method. You can jump to any part of interest following the [Code Architecture-Results](#Code-Architecture).

3. 16 GB GPU memory is preferred for reproducing results of complicated models based on GCN, and at least 24 GB GPU memory for complicated models on GAT. Hardwares we used includes NVIDIA Tesla P100-16GB and NVIDIA GeForce RTX 3090-24GB.

4. **Notice**: There is an alarm that play sounds every time a model is finished training and evaluated. Please disable the code [Implementation-Functions-Alarm](#Code-Architecture) if you find it disturbing.

# Code Architecture

    .
####    ├── Implementation
    │   ├── Import Pakages
    │   ├── Dataset
    │   ├── Data Visualization
    │   ├── Initialization
    │   ├── Logger
    │   ├── Models
    |   │   ├── GCN
    |   │   ├── GAT
    |   │   ├── Residual_GCN
    |   │   └── Residual_GAT
    │   └── Functions
    |       ├── Alarm
    |       ├── Data Preprocess
    |       ├── Node2Vec
    |       └── Main
####    ├── Results
    │   ├── GCN
    |   │   ├── GCN
    |   │   ├── Residual_GCN
    |   │   ├── Residual_GCN+Node2Vec
    |   │   ├── Residual_GCN+Node2Vec+Label_Reuse
    |   │   ├── Residual_GCN+C&S
    |   │   └── Residual_GCN+Node2Vec+Label_Reuse+C&S
    |   └── GAT
    |       ├── GAT
    |       ├── Residual_GAT
    |       ├── Residual_GAT+Node2Vec
    |       ├── Residual_GAT+Node2Vec+Label_Reuse
    |       ├── Residual_GAT+C&S
    |       └── Residual_GAT+Node2Vec+Label_Reuse+C&S
    └── End
