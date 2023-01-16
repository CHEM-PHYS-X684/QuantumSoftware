# Postulate 6

>The time evolution of the state vector $\ket{\psi(t)}$ is governed by the Schrödinger equation:
> $$i\hbar\frac{d}{dt}\ket{\psi(t)} = \hat{H}(t)\ket{\psi(t)},$$

### Time independent case

Imagine the case where $\hat{H}(t) \neq f(t)$. This is just a statement that the Hamiltoninan operator doesn't change in time. 
If that is the case, then we can directly integrate this differential equation, to get the following solution:

$$\begin{align}
\ket{\psi(t)} =& e^{\frac{-i}{\hbar}\hat{H}(t-t_0)}\ket{\psi(t_0)} \\
=& U(t,t_0)\ket{\psi(t_0)}
\end{align}
$$

Differentiate this wavefunction to convince yourself that this is a solution to the time dependent Schrödinger equation.  

Because of this simple form, we can do fancy things, like first go to $t_1$, then go to $t_2$, e.g., 

$$\begin{align}
\ket{\psi(t_2)} = U(t_2,t_1)U(t_1,t_0)\ket{\psi(t_0)}
\end{align}
$$

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
- [Up](/README.md)