# Rabi Interferometry

## Summary

$$
H = \sigma_0r_0+ \vec{\sigma}\cdot\vec{r}
$$

$$
P_{i\to f}(t) = |\langle f|e^{-iHt}|i\rangle|^2
$$

$$
|i\rangle = |0\rangle, \, |f\rangle = |1\rangle
$$

$$
P_{0\to 1}(t) = \sin^2\theta\sin^2{rt} 
$$

### Rabi Frequency

$$
\nu_R = \frac{(\lambda_1 - \lambda_2)}{2} = r
$$

### $\Pi$-Pulse

$$
t_\pi = \frac{\pi}{(\lambda_1 - \lambda_2)}
$$

$$
P_{0\to 1}(t_\pi) = \sin^2\theta
$$

If $\sin\theta = 1$, then $P_{0\to 1}(t) = 1$ (spin flip!)

## Physics

We seek to determine the difference in the energy levels of a qubit.
We couple it to a magnetic field and interrogate it with a laser.

The total magnetic field is:

$$
\vec{B}(t) = B_0 \hat{z} + B_1\cos(\omega t) \hat{x}
$$

So that the Hamiltonian is:

$$
H(t) = -\vec{\mu}\cdot\vec{B}(t) = -\frac{\omega_0}{2}\sigma_z + \omega_1\cos(\omega t)\sigma_x
$$

We make use of the Rotating Wave Approximation so that the Hamiltonian becomes:

$$
H(t) = -\frac{\omega_0}{2}\sigma_z + \omega_1\cos(\omega t)\sigma_x + \omega_1\sin(\omega t)\sigma_y
= \left(
    \begin{matrix}
        \omega_0 & \omega_1 e^{i\omega t} \\
        \omega_1 e^{-i\omega t} & -\omega_0
    \end{matrix}
\right)
$$

If the energy levels of the qubit are $E_0$ and $E_1$ for $|0\rangle$ and $|1\rangle$ respectively, then the Hamiltonian would be:

$$
H_0 = \left(
    \begin{matrix}
    E_1 & 0 \\
    0 & E_0
    \end{matrix}
\right) 
$$

Which we re-write to be:

$$
H_0 = \left(
    \begin{matrix}
    \frac{(E_1 + E_0)}{2} - \frac{E_0 - E_1}{2} & 0 \\
    0 & \frac{(E_1 + E_0)}{2} - \frac{E_1 - E_0}{2}
    \end{matrix}
\right) 
=
\left(
    \begin{matrix}
    \frac{(E_1 + E_0)}{2} + \frac{\Delta}{2} & 0 \\
    0 & \frac{(E_1 + E_0)}{2} - \frac{\Delta}{2}
    \end{matrix}
\right)
$$

That is,

$$
H_0 = \frac{\Delta}{2}\sigma_z + \mathrm{constant}
$$

Where $\Delta$ is the energy splitting that we are looking for.
By applying $H(t)$, we get

$$
H_{tot}(t) = H(t) + H_0 = 
\left(
    \begin{matrix}
        \frac{\Delta - \omega_0}{2} & \omega_1e^{i\omega t}\\
        \omega_1e^{-i\omega t} & -\frac{\Delta + \omega_0}{2}
    \end{matrix}
\right)
$$

If we move into the rotating frame so that

$$
\Phi(t) = 
\left(
    \begin{matrix}
    e^{-i\omega t/2} & 0 \\
    0 & e^{i\omega t/2}
    \end{matrix}
\right)\Psi(t)
$$

Note that this amounts to a unitary transformation of the Hamiltonian $H(t) = U(t)\tilde{H}U^{\dagger}(t)$

$$
U(t) =  
\left(
    \begin{matrix}
    e^{-i\omega t/2} & 0 \\
    0 & e^{i\omega t/2}
    \end{matrix}
\right)
$$

Then we can solve the Schrodinger equation as if the Hamiltonian was time-independent

$$
\tilde{H}\Phi = i\frac{\partial}{\partial t}\Phi
$$

$$
\tilde{H} = 
\left(
    \begin{matrix}
    \frac{\Delta-\omega}{2} & \omega_1\\
    \omega_1 & \frac{-\Delta+\omega}{2}
    \end{matrix}
\right) 
=
-\left(\frac{\Delta-\omega}{2}\right)\sigma_z + \omega_1\sigma_x
$$

Now we can use the [general evolution formula](Two%20Level%20Systems.md) to compute the final state:

$$
r = \sqrt{\omega_1^2 + \frac{1}{4}(\Delta - \omega)^2}\\
\tan\theta = \left(\frac{2\omega_1}{\Delta - \omega}\right)\\
\phi = \arctan(0) = 0
$$

$$
\theta_0 = \pi, \, \phi_0 = 0
$$

$$
|\Phi(t)\rangle = 
i\sin(rt)\sin(\theta)|\tilde{1}\rangle
-
\left[\cos(rt) + i\sin(rt)\cos\theta\right]|\tilde{0}\rangle
$$

Where 

$$
\sin\theta = \frac{\omega_1}{r}, \, \cos\theta = \frac{\Delta-\omega}{2r}
$$

And to transform back to the laboratory frame:

$$
|\tilde1\rangle = e^{-i\omega t}|1\rangle \\
|\tilde 0\rangle = e^{i\omega t}|0\rangle
$$

So that the final solution is:

$$
|\Psi(t)\rangle = 
i\sin(rt)\sin(\theta)e^{-i\omega t}|1\rangle
+
\left[\cos(rt) + i\sin(rt)\cos\theta\right]e^{i\omega t}|0\rangle
$$

Note that when $\Delta = \omega$, $P_{0\to 1}(t) = \sin^2rt$