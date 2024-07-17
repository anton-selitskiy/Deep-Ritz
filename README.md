This repositorium contains the code for the article *Deep Ritz Method for Elliptic Differential-Difference Equations* by Anton Selitskiy. It contains three Jupytor notebooks corresponding to the examples in the paper.

**Example 1.** was calculated with file `DeepRitz_D_1D.ipynb`  

**Example 2.** was calculated with file `DeepRitz_D_Square.ipynb`

**Example 3.** was calculated with file `DeepRitz_D_Circle.ipynb`

For each iteration we samlpe # Samples points from the domain to approximate the energy integral (see the table below).

| Example        | **# Layers** | **# Samples** | $\|u-u_\theta\|_{C(Q)}$ |
|----------------|--------------|---------------|-----------------------------|
| 1D             | 14           | 1600          | 0.009                       |
| 2D rectangular | 30           | 8192          | 0.01                        |
| 2D circle      | 30           | 8192          | --------------------------                         |

For each example we did 10,000 iterations with Adam optimiser with defauld paramiters (learning rate 0.001) and then 10,000 iterations with learning rate 0.0001.
