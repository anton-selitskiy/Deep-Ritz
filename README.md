This repositorium contains the code for the article *Deep Ritz Method for Elliptic Differential-Difference Equations* by Anton Selitskiy. It contains three Jupytor notebooks corresponding to the examples in the paper.

Each file contains:
- A function `exact_solution` is defined, that returns the solution $w$ and a function `reconstr` that returns $u = R_Q^{-1}w$. (For Examples 1 and 2 only.)
- A function `right_hand_side` that returns the right-hand side $f$.
- The model class `ResidualModel`.
- A function `FQ` continues an input function by zero and multiplies it by $\alpha(x)$.
- A function `RQ` that returns $(R_Qu)(x)$ --- the result of the difference operator applied to the function $u(x)$.
- A training loop and the plot of the solution.

For each iteration we samlpe # Samples points from the domain to approximate the energy integral (see the table below).

| Example        | **# Layers** | **# Samples** | $\|u-u_\theta\|_{C(Q)}$ |
|----------------|--------------|---------------|-----------------------------|
| 1D             | 14           | 1600          | 0.009                       |
| 2D rectangular | 30           | 8192          | 0.01                        |
| 2D circle      | 30           | 8192          | --------------------------                         |

For each example we did 10,000 iterations with Adam optimiser with defauld paramiters (learning rate 0.001) and then 10,000 iterations with learning rate 0.0001. The resuted plots look as follows.

**Example 1.** was calculated with file `DeepRitz_D_1D.ipynb`  
![](/img1.png)

**Example 2.** was calculated with file `DeepRitz_D_Square.ipynb`
![](/img2.png)

**Example 3.** was calculated with file `DeepRitz_D_Circle.ipynb`
![](/img3.png)

