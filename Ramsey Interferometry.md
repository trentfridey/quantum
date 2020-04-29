# Ramsey Interferometry

Initial state is $|\Psi(0)\rangle = |0\rangle$

Split Rabi method into 3 stages
1. $\frac{\pi}{2}$ pulse
2. background magnetic field for time $\tau$
3. $\frac{\pi}{2}$ pulse

## The First Stage
The Hamiltonian for the first stage is:

$$
H_1 = -\frac{\Delta}{2}\sigma_z + \omega_1\cos(\omega t)\sigma_x
$$

i.e. the Rabi Hamiltonian, so we can use the same methods for solving it.

The effect of a $\frac{\pi}{2}$-pulse is to rotate the initial Bloch vector $|0\rangle$ by $\frac{\pi}{2}$ radians about the $x$-axis.
Therefore the final state is $|\Psi(\frac{\pi}{2})\rangle = |+y\rangle$

## The Second Stage

The Hamiltonian for the second stage is free precession in the background field:

$$
H_0 = -\frac{\Delta}{2}\sigma_z
$$

With the initial state taken to be the final state from the first stage, i.e., $|+y\rangle = \frac{1}{\sqrt{2}}(|1\rangle+i|0\rangle)$

The final state is (after a time $\tau$):

$$
\left|\Psi\left(\frac{\pi}{2} + \tau\right)\right\rangle = \frac{1}{\sqrt{2}}\left(e^{i\Delta \tau}|1\rangle + i|0\rangle\right)
$$

## The Third Stage

The Hamiltonian for the third stage is the same as the first. 
The only difference is that the initial state is given by the final state of the second state.

We've seen that the effect of a $\pi/2$-pulse on the $|0\rangle$ state is to send it to $|+y\rangle$.
Then to compute the final state we just need to know the effect of a $\pi/2$ pulse on the $|1\rangle$ state.

## Ramsey Fringes

$$
P_{0\to 1}(\tau)
$$