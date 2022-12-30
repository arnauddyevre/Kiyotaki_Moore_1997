# Numerical solution of Kiyotaki & Moore (1997) "Business Cycles".

Jupyter and Google Colab notebooks reproducing the numerical solution of Kyotaki & Moore (1997). This Notebook reproduces Figure 3 of the paper (available in the doc folder). It uses a shooting algorithm to find the Initial Value Condition that reproduces the cyclicality of the full non-linear model, while converging to the steady state in the long run.

### 1. Model equations

*(1) Land market equilibrium condition*
$$q_{t+1}= R(q_{t} - u\left(K_{t}\right))$$

*(2) Law of motion of the farmers' aggregate landholding*
$$\begin{equation}
K_{t}=(1-\pi) \lambda K_{t-1} +\frac{\pi}{\phi + q_t - \frac{1}{R} q_{t+1}}\left[\left(a+q_{t}+\lambda \phi\right) K_{t-1}-R B_{t-1}\right]
\end{equation}$$

*(3) Law of motion of the farmers' aggregate debt*
$$B_{t}=R B_{t-1}+q_{t}\left(K_{t}-K_{t-1}\right)+\phi\left(K_{t}-\lambda K_{t-1}\right)-a K_{t-1}$$

Where:
