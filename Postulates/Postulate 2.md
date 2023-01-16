# Postulate 2

>Every measurable quantity A is described by a Hermitian operator $\hat{A}$. 

Do you want to know what a system's energy is? Apply the energy operator, this is referred to as the `Hamiltonian` operator, $\hat{H}$. What's the magnetization? Apply the magnetization operator, etc. 

#### Ising example: 

Remember that we defined our energy with the following energy function:
$$E(\textbf{s}) = -\frac{J}{k_B}\sum_{\langle ij\rangle}s_is_j + \frac{\mu}{k_B}\sum_is_i$$
We can define the associated operator to be: 
$$\hat{H} = -\frac{J}{k_B}\sum_{\langle ij\rangle}\sigma^Z_i \sigma^Z_j + \frac{\mu}{k_B}\sum_i \sigma^Z_i$$
where $\sigma^Z_i$ is the 

$$\begin{pmatrix} 1 & 0 \\\ 0 & -1 \end{pmatrix}$$ 

matrix applied to the $i^\text{th}$ qubit.

For example:

$$\begin{align}
\sigma^Z_1 \ket{0} &= \ket{0} \\
\sigma^Z_1 \ket{1} &= -\ket{1} 
\end{align}$$

This is seen by simple matrix-vector multiplication. Recall that we defined:

$$\begin{align}
\ket{0} = \begin{pmatrix}1 \\\ 0\end{pmatrix} \\
\ket{1} = \begin{pmatrix}0 \\\ 1\end{pmatrix}
\end{align}$$

If we have multiple qubits, then the subscript just tells you which qubit to apply the operator to. 

$$\begin{align}
\sigma^Z_1 \ket{01} &= \ket{01} \\
\sigma^Z_1 \ket{11} &= -\ket{11} \\
\sigma^Z_2 \ket{01} &= -\ket{01} \\
\sigma^Z_2 \ket{10} &= \ket{10} 
\end{align}$$

- [Previous](<Postulate 1.md>)
- [Next](<Postulate 3.md>)

