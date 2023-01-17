## Calculus

- [Derivative](https://en.wikipedia.org/wiki/Derivative)
- [Integral](https://en.wikipedia.org/wiki/Integral)
- [Limits](https://en.wikipedia.org/wiki/Limit_(mathematics))
- [Taylor Series](https://en.wikipedia.org/wiki/Taylor_series)
  
  The general definition of a Taylor series of a function of $x$, is given as:
	$\displaystyle f(a) = \sum_{n=0}^\infty f^{(n)}(a)\frac{\left(x-a\right)^n}{n!},$
	which results in a polynomial in $x$, where the $n^{th}$ order  coefficient of the polynomial is the $n^{th}$ order derivative. 

## Vectors

### Three Dimensions
In 3D, [vectors](https://en.wikipedia.org/wiki/Euclidean_vector) are simply directional quantities, a geometric object with both a direction and a magnitude. We can denote them as:

$$
\vec{v} = v_x\vec{x} + v_y\vec{y} + v_z\vec{z}.
$$

If we add two vectors, we simply add their coefficients:

$$
\vec{v} + \vec{w} 
=\left(v_x + w_x\right)\vec{x} 
+\left(v_y + w_y\right)\vec{y}
+\left(v_z + w_z\right)\vec{z}
$$

and multiplying vectors can be defined in one of 2 ways: the inner product, and the outer product. 

The [inner product](https://en.wikipedia.org/wiki/Dot_product) (or dot product, or scalar product) is simply written as:

$$
\vec{v}\cdot\vec{w} = \sum_{i=1}^3v_iw_i = v_1w_1 + v_2w_2 + v_3w_3
$$

As you probably remember from earlier math classes, the dot product is:

$$
\vec{v}\cdot\vec{w} = \lVert\vec{v}\rVert\cdot\lVert\vec{w}\rVert\cos{\theta},
$$

where $\theta$ is just the angle between the two vectors. Notice that the dot product is bounded between zero and the product of the magnitudes:

$$
\lVert\vec{v}\cdot\vec{w}\rVert \leq \lVert\vec{v}\rVert\cdot\lVert\vec{w}\rVert.
$$

This is referred to as the [Cauchy-Schwartz Inequality](https://en.wikipedia.org/wiki/Cauchy%E2%80%93Schwarz_inequality). Once the basis vectors (i.e., $\vec{x}$, $\vec{y}$, $\vec{z}$) are specified, the vector $\vec{v}$ can be fully defined by only specifying its coefficients:

$$
\vec{v} = 
\left(
\begin{array}{c}
v_x \\ v_y \\ v_z
\end{array}
\right)
$$

in this notation we can also define a dot product as:

$$
\vec{v}\cdot\vec{w} = \vec{v}^\dagger\vec{w} = 
\left(\begin{array}{c}
v_x & v_y & v_z
\end{array}\right)
\left(\begin{array}{c}
w_x \\ w_y \\ w_z
\end{array}\right)
$$

where the $\dagger$ indicates an adjoint, or [transpose](https://en.wikipedia.org/wiki/Transpose) when the vector is real. 


### N-dimensions
We can generalize this to an arbitrary number of dimensions. When we do so, we usually drop the $\rightarrow$ decoration, in favor of Dirac's [Braket notation](https://en.wikipedia.org/wiki/Bra%E2%80%93ket_notation), where vectors are denoted as a label inside of a "ket", $\vec{v}\rightarrow\ket{v}$.  
Using this notation, we can take any given basis $\{\ket{v_1}, \ket{v_2}, \dots, \ket{v_i}\}$ of dimension $N$, and write an arbitrary function directly in terms of it's coefficients:
 
$$
\ket{\sigma} = \sum_{i=1}^Nc_i\ket{v_i}.
$$

A vector can be thought of as a discretized function. For instance, the $i^{th}$ component of a vector returns a number. Similarly, if we pass $i$ to the function $f(x)$ we also get a number back. 

In this form, the dot product (now consistently referred to as the inner product) is written as:[^cc]

$$\braket{v\vert w} = \left(\ket{v}\right)^\dagger\cdot\ket{w} = \sum_i v_i^*w_i
$$

Notice that the inner product returns a `scalar`, or a simple number. Because of this, the inner product is also referred to as the scalar product. 
However, as mentioned above, there are two ways to multiply two vectors. In addition to the inner product discussed above, we also can define an [outer product](https://en.wikipedia.org/wiki/Outer_product). Assume $\ket{v}$ is $N$-dimensional, and $\ket{w}$ is $M$-dimensional (note, that $N=M$ is certainly possible and allowed), then:

$$
\ket{v}\otimes\ket{w} = \begin{pmatrix}
v_1w_1 & v_1w_2 & v_1w_3 & \cdots & v_1w_M \\
v_2w_1 & v_2w_2 & v_2w_3 & \cdots & v_2w_M \\
v_3w_1 & v_3w_2 & v_3w_3 & \cdots & v_3w_M \\
\vdots & \vdots & \vdots & \ddots & \vdots \\ 
v_Nw_1 & v_Nw_2 & v_Nw_3 & \cdots & v_Nw_M \\
\end{pmatrix}.
$$

So whereas the `inner product` gives us a scalar, the `outer product` gives us a [matrix](https://en.wikipedia.org/wiki/Matrix_(mathematics))!

[^cc]:	Here (and throughout this course) we will assume that the basis vectors form an orthonormal set. This simply means that the inner product of a vector with itself $\braket{v_i\vert v_i} = 1$ and the inner product with any other vector is zero, $\braket{v_i\vert v_j} = 0$, when $i\neq j$. 

## Matrices

Matrices, as you probably remember from linear algebra, are 2D grids of numbers. Whereas vectors can be thought of as *discretized functions*, matrices can be viewed as *discretized operators*. This becomes more evident after considering the multiplication of a vector by a matrix:

$$
\left(
\begin{array}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{array}
\right)
$$

## Dirac Notation

## Resolution of the identity
## Eigensystems
- [Wikipedia](https://en.wikipedia.org/wiki/Eigendecomposition_of_a_matrix)
## Matrix exponential 
Assume $\hat{A}$ is a Hermitian matrix (this isn't necessary but it's helpful here). We can define the matrix exponential with standard [Taylor Series](https://en.wikipedia.org/wiki/Taylor_series#Exponential_function):

$\displaystyle e^{\hat{A}} = \hat{I} + \hat{A} + \frac{1}{2!}\hat{A}^2 + \frac{1}{3!}\hat{A}^3 + \cdots$

While this is formally straightforward, it's not clear how we would compute it in practice. To do so, we can simply use the eigendecomposition, $\hat{A} = \hat{U}a\hat{U}^\dagger$, where $a$ is a diagonal matrix of eigenvalues. 