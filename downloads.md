---
layout: page
title: Downloads
permalink: /downloads/
---

# Benchmarking Separability-Entanglement Classifier

## Datasets

The dataset of our paper is available [here](/downloads/ent_data.zip). Both qubit and qutrit cases are included. You may test it, or even try to further improve our result with any other machine learning method you want.

## Program

We provide program in MATLAB for you to generate data and test for youself. You may download it [here](/downloads/entlib_sources.zip). Explanations are available below

### List of Functions

#### RandomState

**RandomState** is a function that generates a random density matrix. 

##### Syntax

`state = RandomState(dim, lambda)`

##### Argument Descriptions

- `dim`: the number of rows (columns) the density matrix will have.
- `lambda`: The parameter $$\lambda$$. When generating an $$n \times n$$ density matrix, we first pick $$d_1, \ldots, d_n$$ on the simplex $$\sum_{i=1}^n d_i = 1$$ under the Dirichlet distribution $$\Delta_{\lambda}(d_1, \ldots, d_n) = C d_1^{-\lambda} \ldots d_n^{-\lambda},$$ where $$C$$ is the normalization constant.

#### DMtoVector

**DMtoVector** is a function that transform a density matrix to a generalized bloch vector.

##### Syntax

`vector = DMToVector(rho)`

##### Argument Descriptions

- `rho`: the density matrix that we wish to transform.

#### Alpha

Given a point $$\mathbf{p} \in \mathbb{R}^d$$ and a set of extreme points $$P_1, \ldots, P_n \in \mathbb{R}^d$$ of a convex hull $$\mathcal{CH} = \textrm{conv}(P_1, \ldots, P_n)$$ such that $$\mathbf{0} \in \mathcal{CH}$$, **Alpha** computes the maximum $$\alpha$$ such that $$\alpha\mathbf{p} \in \mathcal{CH}$$.

##### Syntax

`alpha = Alpha(p, extreme)`

##### Argument Descriptions

- `p`: the point $$\mathbf{p}$$, which is a $$d$$-by-$$1$$ matrix.
- `extreme`: the points $$P_1, \ldots, P_n$$, which is an $$n \times d$$ matrix.