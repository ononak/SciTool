# SciTool

SciTool is a library containing various algorithms for scientific applications.  


## Regularization

Regularization is a method to adjust how closely a model fits to data. Adding an additional term that penalizes the loss function is one of the ways of adjusting the output model.
Linear regularization problems can be defined as follows.

![equation](https://github.com/ononak/SciTool/assets/17129016/e6623a28-9465-428a-9ea9-3986f7902d15)

<!-- $\min_{\mathbf{x} \in \mathbb{R}^{n}}\{\frac{1}{p}\|\mathbf{y} - \mathbf{A}\mathbf{x}\|_{p}^{p} + \frac{\lambda^{2}}{q}\|\mathbf{L}\mathbf{x}\|_{q}^{q}\} \quad \quad 0 < p,q \leq 2 \quad \mathbf{A} \in \mathbb{R}^{m \times n} \quad \mathbf{y} \in \mathbb{R}^{m} \quad \mathbf{L} : \mathbb{R}^{m} \rightarrow \mathbb{R}^{s}$ -->
  
Here, $p$ and $q$ represent the norm of the vectors. $\mathbf{x}$ is the unknown source (or the model parameters) to be estimated, $\mathbf{A}$ is the forward model matrix with high condition number or it is rank deficient. $\mathbf{L}$ is the regularization operator, which is used to adjust the properties of the output model. $\lambda$ is a regularization parameter employed to determine the weight of the regularization term in the solution. $\mathbf{y}$ is the noisy measurements that can be expressed as follows;

$\mathbf{y}= \mathbf{A}\mathbf{x} + \mathbf{n}$

Where $\mathbf{n}$ is the measurement noise vector.

- If $p = q = 2$, then the problem is called Tikhonov regularization or $L_{2}$ regularization that usually yields smooth estimation.

- If $p = 2$, $q = 1$, then the problem is called $L_{1}$ regularization, which promotes sparsity in the solution.

***Reference:*** A Generalized Krylov Subspace Method for $L_{p}L{q}$ Minimization A. Lanza et al [doi:10.1137/140967982](https://epubs.siam.org/doi/10.1137/140967982) 

## Kalman Filter

Kalman filtering is an algorithm that allows us to estimate the state of a system based on observations or measurements.
![Kalman](https://github.com/ononak/SciTool/assets/17129016/3728fe3d-11d6-434f-bd87-504838daff51)
