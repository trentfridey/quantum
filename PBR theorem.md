PBR theorem

Authors: Pusey, Barrett, Rudolph
[Arxiv PDF](https://arxiv.org/pdf/1111.3328v1.pdf)

## Summary

What does a (pure) quantum state represent?
Either:
 - physical property of a system
 - only statistical significance

Given assumptions, the statistical interpretation is not consistent with the predictions of quantum theory.

## No-Go Theorem

If the quantum state merely represents information about the real physical state of a system, then experimental predictions are obtained which contradict those of quantum theory.

## Assumptions

1. The system has a real physical state -- objective and independent of the observer. Only necessary for isolated systems.

2. Systems that are prepared independently have independent physical states.

## Refinement

### Classical Mechanics
In Classical Mechanics, point particle described by $(x,p)$ in phase space. 
Other physical properties are functions of these.
Uncertainty captured by probability distribution $\mu(x,p)$ evolving under Liouville's equation.

### Quantum Mechanics
Hypothesis: Quantum state is a state of knowledge, representing uncertatinty of real physical state ($\lambda$). 
Preparing a pure state $|\psi\rangle$ does not necessarily fix $\lambda$, but yields $\mu_\psi(\lambda)$.
If another $\mu_\phi(\lambda)$ has overlapping support with $\mu_\psi(\lambda)$, then $\psi$ cannot be a physical property.

## Argument

### When $\langle \phi_0 | \phi_1 \rangle = 1/\sqrt{2}$

Proof by contradiction:

1. Choose basis so that $|\phi_0\rangle = |0\rangle$ and $|\phi_1\rangle = |+\rangle$
2. Assume that the complete physical state $\lambda$ is compatible with either preparation method.
3. Assume for either method the probability of (2) happening is at least $q > 0$.
4. Let the two physical states $\lambda_1$ and $\lambda_2$ be uncorrelated. 
5. Then with probability $q^2 > 0$, the physical states $\lambda_1$ and $\lambda_2$ are compatible with any of the four possible preparations: $|0\rangle \otimes |0\rangle$, $|0\rangle \otimes |+\rangle$, $|+\rangle \otimes |0\rangle$, $|+\rangle \otimes |+\rangle$
6. The two systems are measured by a device that is only determined by the complete physical state of the two systems at the time of measurement.
7. The measurement projects onto four orthogonal states which indicate not 00, not +0, not 0+, not ++, i.e. that quantum theory predicts should happen with probability $0$
8. At least $q^2$ of the time, the measuring device will be uncertain which of the four possible preparation methods was used, which means it would give an outcome that quantum theory predicts should occur with probability $0$. $\Rightarrow\Leftarrow$
9. Hence, no physical state $\lambda$ of the system can be compatible with both of the quantum states $|0\rangle$ and $|+\rangle$.
10. If the same can be shown for any pair $|\phi_0\rangle$ and $|\phi_1\rangle$, then the quantum state can be inferred uniquely from $\lambda$.
11. Therefore the quantum state is a physical property of the system and the statistical view is false. $\blacksquare$

### Arbitrary $|\phi_0\rangle, \, |\phi_1\rangle$ 

Let 

$$
|\phi_0\rangle = \cos{\theta/2}|0\rangle - \sin{\theta/2}|1\rangle \\
|\phi_1\rangle = \cos{\theta/2}|0\rangle + \sin{\theta/2}|1\rangle \\
0 < \theta < \pi/2
$$ 

be states in a two-dimensional subspace of the Hilbert space.
Then we prepare $n$ uncorrelated systems, with each system in either state.
If there is a joint measurement on the $n$ systems with $2^n$ outcomes such that each outcome has probability zero on at least one of the $|\Psi(x_1,...,x_n)\rangle$