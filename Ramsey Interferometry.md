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

With the initial state as $|\psi(0)\rangle = |0\rangle$.
Since this is the same as the Rabi Hamiltonian, we can use the same techniques here to solve for the final state.
We can use the general evolution formula to compute the final state (in the rotating frame):

$$
|\Psi(\pi/4r)\rangle = 
i\frac{1}{\sqrt{2}}\sin\theta |1\rangle
+
\left[\frac{1}{\sqrt{2}} + i\frac{1}{\sqrt{2}}\cos\theta\right]|0\rangle
$$

Or in the case of $\Delta = \omega$:

$$
|\Psi(\pi/4r)\rangle = 
i\frac{1}{\sqrt{2}}|1\rangle
+
\frac{1}{\sqrt{2}}|0\rangle
= |+y\rangle
$$


## The Second Stage

The Hamiltonian for the second stage is free precession in the background field:

$$
H_0 = -\frac{\Delta}{2}\sigma_z
$$

With the initial state taken to be the final state from the first stage, i.e., 
$$
|\Psi(\pi/4r)\rangle = \frac{1}{\sqrt{2}}\left( i|1\rangle
+
|0\rangle\right)
$$

The final state is (after a time $\tau$):

$$
\left|\Psi\left(\frac{\pi}{4r} + \tau\right)\right\rangle = \frac{1}{\sqrt{2}}\left(i|1\rangle + e^{-i\Delta \tau}|0\rangle\right)
$$

## The Third Stage

The Hamiltonian for the third stage is the same as the first. 
The only difference is that the initial state is given by the final state of the second state.

Using the [formula for the general solution](Two%20Level%20Systems.md), we have

$$
r = \sqrt{\omega_1^2 + \frac{1}{4}\left(\Delta-\omega\right)^2}\\
\theta = \arctan\frac{2\omega}{\Delta - \omega} = \pi/2,
\, \phi = 0\\
\theta_0 = \frac{\pi}{2}, 
\, \phi_0 = -\Delta \tau - \pi/2
$$

$$
\left|\Psi\left(\frac{\pi}{2r} + \tau\right)\right\rangle = 
\left(\frac{e^{-i\Delta t}}{2} 
+ \frac{1}{2}\right)|1\rangle
+
i\left(\frac{e^{-i\Delta t}}{2} - \frac{1}{2}\right)|0\rangle
$$

## Ramsey Fringes

Note that $\Delta = \omega$

$$
\boxed{
P_{0\to 1}(\tau) 
= \left|\left\langle 1|\Psi\left(\frac{\pi}{2r} + \tau\right)\right\rangle\right|^2 
= \cos^2\frac{\Delta \tau}{2}
}
$$