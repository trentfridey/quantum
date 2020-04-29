Rotating Wave Approximation

## Origin 

We can change the linearly polarized laser field:

$$
\vec{B}_1(t) = \cos(\omega t)\hat{x}
$$

into a circularily polarized laser field:

$$
\vec{B}_2(t) = \cos(\omega t)\hat{x} + \sin(\omega t)\hat{y}
$$

Hence "Rotating Wave". Now

$$
\cos(\omega t) = \frac{1}{2}(e^{i\omega t} + e^{-i\omega t}) = \frac{1}{2}e^{i\omega t}(1+e^{-2i\omega t})
$$

For $\omega \gg 1$:

$$
(1+ e^{-2i\omega t}) \approx 2
$$

Hence "Approximation"

## Application

The Hamiltonian for the Rabi method for qubit spectroscopy is:

$$
H = 
-\frac{\Delta}{2}\sigma_z + \omega_1\cos(\omega t)\sigma_x
\\ \Longrightarrow_{RWA}
\\ \approx
\left(
    \begin{matrix}
    -\Delta/2 & \omega_1 e^{i\omega t}\\
    \omega_1 e^{-i\omega t} & \Delta/2
    \end{matrix}
\right)
$$
