# Postulate 6

>The time evolution of the state vector $\ket{\psi(t)}$ is governed by the Schrödinger equation:
> $$i\hbar\frac{d}{dt}\ket{\psi(t)} = \hat{H}(t)\ket{\psi(t)},$$

It is often helpful  at this point to introduce what we call the Unitary Time Evolution Operator, $\hat{U}(t,t_0)$. The TEO is just an operator that transforms (or "evolves") our system from some initial time, $t_0$, to a final time, $t$. For instance,
$$\ket{\psi(t)} = \hat{U}(t,t_0)\ket{\psi(t_0)}.$$
At this point, we don't yet care about the actual form of the operator, just that it must be `unitary`. The reason for it's unitarity is simple to see. As postulate 1 state, the coefficients of the wavefunction are the probabilities of observing a specific state. Because all probabilities must add to 1, the norm of the wavefunction must remain normalized. This is true for both $t_0$ and $t$, and for all times in between. The property that a matrix applied to a vector preserves its norm is exactly the property of unitarity. As such, the only restriction we impose on the TEO is that it must be unitary.

Substituting this into the Schrodinger equation gives, 
$$i\hbar\frac{d}{dt}\hat{U}(t,t_0)\ket{\psi(t_0)} = \hat{H}(t)\hat{U}(t,t_0)\ket{\psi(t_0)}.$$
Because this equation is true for any possible starting point, it must hold for the TEO itself,
$$\frac{d}{dt}\hat{U}(t,t_0) = -\frac{i}{\hbar}\hat{H}(t)\hat{U}(t,t_0).$$
This is a useful (yet equivalent) form of the time dependent Schrodinger equation.

### Time independent case

First let us start with the simplest case, that where $\hat{H}(t) = \hat{H} \neq f(t)$. This is just a statement that the Hamiltonian operator doesn't change in time. 
$$\frac{d}{dt}\hat{U}(t,t_0) = -\frac{i}{\hbar}\hat{H}\hat{U}(t,t_0).$$
For this situation, we can directly integrate the differential equation. To do so, we can recognize that when we differentiate the TEO, we get it back times the Hamiltonian. Exponential functions are known to have this property. Simple substitution shows that the following form provides a solution to the TDSE for static Hamiltonians:
$$\hat{U}(t,t_0) = e^{\frac{-i}{\hbar}\hat{H}(t-t_0)}. $$
Differentiate this to convince yourself that this is a solution to the time dependent Schrödinger equation.  Because of this simple form, we can do fancy things, like first go to $t_2$, then go to $t$, e.g., 
$$\ket{\psi(t)} = U(t,t_2)U(t_2,t_0)\ket{\psi(t_0)}$$
such that 
$$U(t,t_0) = U(t,t_2)U(t_2,t_0).$$
We can simplify this a bit. What if we choose $t_2$ to be the midpoint between $t$ and $t_0$, $t_2 = (t-t_0)/2$?
$$
\begin{aligned}
U(t,t_0) &= U(t,t_2)U(t_2,t_0) = e^{\frac{-i}{\hbar}\hat{H}(t-t_2)}e^{\frac{-i}{\hbar}\hat{H} (t_2-t_0)}  \\\\
 &= e^{\frac{-i}{\hbar}\hat{H}(t-t_2)}e^{\frac{-i}{\hbar}\hat{H} (t_2-t_0)}  \\\\
 &= \left(e^{\frac{-i}{\hbar}\hat{H} (t-t_0)/2} \right)^2 
\end{aligned}
$$

We can generalize this,
$$ \begin{aligned}
U(t,t_0) &= \left(e^{\frac{-i}{\hbar}\hat{H} (t-t_0)/N} \right)^N \\\\
\end{aligned}$$
### Time dependent case

The more general (and complicated) case where $\hat{H}$ is time-dependent cannot be written down in such a simple form. However, we can develop an arbitrarily accurate approximation to the solution by using the result above. 
Assume we want to solve for $\ket{\psi(t)}$, we can break up the evolution into _infinitely_ many steps:

$$\begin{align}
\ket{\psi(t)} = \lim_{N\rightarrow \infty} U(t,t_{N-1})\dots U(t_2,t_1) U(t_1,t_0)\ket{\psi(t_0)}
\end{align}$$

By dividing the evolution into small enough time steps, we can use the time independent solution!
The core idea, is that within a small enough time window, $t_i \rightarrow t_{i+1}$, the Hamiltonian is changing slowly enough such that it appears constant. This means that whatever the Hamiltonian looks like at a give time, $\hat{H}(t_i)$, we can exponentiate it, to obtain a unitary $U(t_{i+1}, t_i)$.

In practice, of course, we can never write down a real $\infty$ of terms. And so we simply stop at some point and accept that there is some approximation being made. 

$$\begin{align}
\ket{\psi(t)} \approx   U(t,t_{N-1})\dots U(t_2,t_1) U(t_1,t_0)\ket{\psi(t_0)}
\end{align}$$


- [Previous](<Postulate 5.md>)
- [Up](./README.md)