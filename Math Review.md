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

So whereas the `inner product` gives us a scalar, the `outer product` gives us a [matrix](https://en.wikipedia.org/wiki/Matrix_(mathematics))! This can also be represented with Dirac notation as,

$$
\ket{v}\otimes\ket{w} = \ket{v}\bra{w}
$$


[^cc]:	Here (and throughout this course) we will assume that the basis vectors form an orthonormal set. This simply means that the inner product of a vector with itself $\braket{v_i\vert v_i} = 1$ and the inner product with any other vector is zero, $\braket{v_i\vert v_j} = 0$, when $i\neq j$. 


## Matrices

Matrices, as you probably remember from linear algebra, are 2D grids of numbers. Whereas vectors can be thought of as *discretized functions*, matrices can be viewed as *discretized operators*. This becomes more evident after considering the multiplication of a vector by a matrix:

$$
\begin{pmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{pmatrix} 
\begin{pmatrix}
v_{1}  \\
v_{2}  
\end{pmatrix}
=
\begin{pmatrix}
a_{11}v_{1} + a_{12}v_{2}  \\
a_{21}v_{1} + a_{22}v_{2} 
\end{pmatrix}
=
\begin{pmatrix}
w_{1}  \\
w_{2}  \\
\end{pmatrix}.
$$

As we see, the application of a matrix to a vector returns a new vector. In other words, a matrix transforms a vector into vector, just as an operator (e.g., a derivative) transforms a function into another function.


When we multiply two matrices together, we get:

$$
\begin{pmatrix}
a_{11} & a_{12} \\
a_{21} & a_{22}
\end{pmatrix}
\begin{pmatrix}
b_{11} & b_{12} \\
b_{21} & b_{22}
\end{pmatrix}
=
\left(
\begin{array}{c|c}
a_{11}b_{11} + a_{12}b_{21} & 
a_{11}b_{12} + a_{12}b_{22} \\\hline
a_{21}b_{11} + a_{22}b_{21} & 
a_{21}b_{12} + a_{22}b_{22} \\
\end{array}
\right)
=
\begin{pmatrix}
c_{11} & c_{12} \\
c_{21} & c_{22}
\end{pmatrix}
$$

If a matrix has the property, $\hat{A}^\dagger = \hat{A}$, it is called a . 

A few types of matrices:

| Definition | Name | Common Context | 
|---|---| --- |
|$\hat{A} = \hat{A}^\dagger$ | [Hermitian](https://en.wikipedia.org/wiki/Hermitian_matrix) | Physical Observables | |
|$\hat{A}^\dagger = \hat{A}^{-1}$ | [Unitary](https://en.wikipedia.org/wiki/Unitary_matrix) | Time Evolution |
|$\hat{A}\hat{A} = \hat{A}$ | [Idempotent](https://en.wikipedia.org/wiki/Idempotent_matrix) | Projection |
|$\hat{A}\hat{A} = \hat{I}$ | [Involutory](https://en.wikipedia.org/wiki/Involutory_matrix) | Pauli's/Angular Momentum|


## Resolution of the identity
Above, we saw that while the inner product, $\braket{v\vert w}$, is a scalar, the outer product, $\ket{v}\bra{w}$ is a matrix. Let's take one of our orthonormal basis vectors ($\ket{v_i}$) and inspect the outer product with itself:

$$
\hat{P}_i = \ket{v_i}\bra{v_i}
$$

We call this the `projector` onto the $i^{th}$ vector, a terminology which can be understood by considering it's action upon a vector, $\ket{x} = \sum_jx_j\ket{v_j}$.

$$\begin{align}
\hat{P}_i\ket{x} = &\ket{v_i}\bra{v_i}\sum_jx_j\ket{v_j}\\
 =& \sum_jx_j\ket{v_i}\braket{v_i\vert v_j}\\
 =& \sum_jx_j\ket{v_i}\delta_{ij}\\
 =& x_i\ket{v_i}
\end{align}$$

From this, we can see that applying the $i^{th}$ projector onto any vector will return the component of that vector along the $i^{th}$ direction. To relate back to a 3D case, if we apply the projector for the $x$ axis to any vector we would get back the component along the $x$ axis. 

Intuitively, if we were to apply a  projection twice, it should have the same result as applying it once - once we have projected onto a specific basis vector, there's nothing left to project out. Such a matrix is called [Idempotent](https://en.wikipedia.org/wiki/Idempotent_matrix). 

$$\begin{align}
\hat{P}_i\hat{P}_i =& \left(\ket{v_i}\bra{v_i}\right)\left(\ket{v_i}\bra{v_i}\right)\\
=& \ket{v_i}\braket{v_i|v_i}\bra{v_i}\\
=& \ket{v_i}\bra{v_i}\\
=& \hat{P}_i\\
\end{align}$$

We could also define a projection onto a subspace by just adding the corresponding projectors. Imagine a 3D vector. We could obtain its projection on the $xy$ plane, by simply adding $\hat{P}_x + \hat{P}_y$. Applying this to any 3D vector would essentially give its "shadow" on the $xy$ plane. 

What if we were to add up the projection operators for all the basis vectors? This would give the projection on the full space, which is simply just the original vector. This might seem like a silly thing to do, but it is really useful in Linear Algebra and Quantum Mechanics, and is referred to as the `Resolution of the Identity`. 

$$
\hat{I} = \sum_i\ket{v_i}\bra{v_i}
$$

We can use the resolution of the identity to change from one basis to another. 

## Eigensystems
- [Wikipedia](https://en.wikipedia.org/wiki/Eigendecomposition_of_a_matrix)

Although any operator, $\hat{A}$,  can be multiplied against a vector, $\ket{v}$ to yield a new vector, $\ket{w}, often times one encounters the situation where the transformation of a vector by a matrix is particularly simple in that it only "scales" the vector by a number. When this happens, we refer to the vector as an `eigenvector` of the operator, and the value by which the result is scaled is called the `eigenvalue`. In the following,

$$
\hat{A}\ket{v} = a_v\ket{v}
$$

we would say that $\ket{v}$ is an eigenvector of $\hat{A}$ with eigenvalue, $a_v$. 

For hermitian matrices, we can always find a full set of eigenvectors which is equal to the dimension of the space. Resolving the identity into this basis yields a matrix which is diagonal, and thus this process is called `diagonalizing` the matrix. 

## Matrix exponential 
Assume $\hat{A}$ is a Hermitian matrix (this isn't necessary but it's helpful here). We can define the matrix exponential with standard [Taylor Series](https://en.wikipedia.org/wiki/Taylor_series#Exponential_function):

$\displaystyle e^{\hat{A}} = \hat{I} + \hat{A} + \frac{1}{2!}\hat{A}^2 + \frac{1}{3!}\hat{A}^3 + \cdots$

While this is formally straightforward, it's not clear how we would compute it in practice. To do so, we can simply use the eigendecomposition, $\hat{A} = \hat{U}a\hat{U}^\dagger$, where $a$ is a diagonal matrix of eigenvalues. 