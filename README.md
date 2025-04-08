# HyperPLR: Hypergraph Generation through Projection, Learning, and Reconstruction

## Enverement preparation

1. Clone the repository
    ```
    git clone https://github.com/RKIzmailov/HyperPLR.git
    cd HyperPLR
    ```

2. Create virtual envirement with Python 3.9

    Change the name `hyperplr` if you need
    ```
    conda create -n hyperplr python=3.9
    ```

3. Activate your enverement

    ```
    conda activate hyperplr
    ```

4. Install required dependencies 

    ```
    pip install torch==1.10.2 torchvision==0.2.2
    pip uninstall numpy
    pip install numpy==1.23.5
    pip install torch-scatter==2.0.9 torch-sparse==0.6.14 torch-cluster==1.6.0 torch-spline-conv==1.2.1 --no-deps
    pip install torch-spline-conv==1.2.1 -f https://data.pyg.org/whl/torch-1.10.2+cpu.html
    pip install -r .\requirment.txt
    ```


## The framework

The framework can be found in ``main.ipynb``.

Some related method should be found in utils. (The algorithm ``GWC`` in the paper is implemented by function ``lazy_clique_edge_cover``)


## Dataset

- [Dataset](https://www.cs.cornell.edu/~arb/data/)

## Maximal cliques finding cost

- contact-high-school, 0.06284904479980469
- contact-primary-school, 0.8914539813995361
- email-Enron, 0.011591196060180664
- email-Eu, 3.432471990585327
- NDC-classes, 0.02602386474609375


## Metrics

- hypergraph
  - density
  - average size
  - average degree
- projected graph
  - coefficient
  - modularity
- bipartite graph
  - modularity