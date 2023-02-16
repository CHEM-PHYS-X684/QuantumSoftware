# Postulate 1

> The state of a physical system is defined by a linear combination of all possible configurations. This vector is called a `ket` and is denoted with a bracket: $\ket{\psi}$.

Unlike a classical system, which can only exist in one spin configuration at a time (e.g., $\ket{\uparrow\downarrow\uparrow}$ vs $\ket{\downarrow\uparrow\uparrow}$ or equivalently $\ket{101}$ vs $\ket{011}$) a quantum mechanical system can exist in a `superposition` of all possible configurations. In Dirac notation, that state would be denoted $\ket{\psi}$,  where $\psi$ is just a label for the state (we can use other labels as well when convenient), and can be written as a linear combination of configurations. 

Consequently, if we had a system of 3 *quantum spins*, then we'd have to treat the system accordingly:

$$\begin{align}
\ket{\psi} =& c_0\ket{000} + c_1\ket{001} + c_2\ket{010} \\
		& + c_3\ket{011} + c_4\ket{100} + c_5\ket{101} \\
		& + c_6\ket{110} + c_7\ket{111} \\ 
           =& \sum_I c_I\ket{I},
\end{align}$$

where $I$ denotes a particular configuration, and $c_I$ is the expansion coefficient for the $I^{th}$ configuration. This means that the system is *simultaneously* in multiple configurations. 

#### Probabilities

An interesting feature of quantum mechanics is that each $c_I$ can be a complex number: $c_I = a + bi$.  We interpret each coefficient, $c_I$, to be the probability `amplitude` that the system is the associated configuration, $\ket{I}$. The `probability`, $P_I$, of being in state $\ket{I}$ is therefore given by the coefficient times its complex conjugate: $P_I = c_I^*c_I$ ,  where $^{*}$ denotes a complex conjugate.[^cc] For example, the probability of finding the system in state $\ket{001}$ would simply be $c_1^*c_1$. We have listed out all possible configurations, so the system must be in one of them. In other words, if we add up the different probabilities, we should get 1. 

$$\sum_I P_I = \sum_I c_I^*c_I = 1.$$

[^cc]:	Here we introduced the notation of a `complex conjugate`. The complex conjugate, simply returns the same number, but with the imaginary component multiplied by a negative sign. For example, $(a+bi)^* = a-bi$, where $i=\sqrt{-1}$.


- [Previous](Postulates/README.md)  
- [Next](<Postulate 2.md>)


