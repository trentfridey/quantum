Two Level Systems

# Two Level Systems

## General Hamiltonian

$$
H = \sigma_0r_0+ \vec{\sigma}\cdot\vec{r}
$$

$\vec{r} = r\cos\phi\sin\theta\hat{x} + r\sin\phi\sin\theta\hat{y} + r\cos\theta\hat{z}$

$\vec{\sigma} = \sigma_x\hat{x} + \sigma_y\hat{y} + \sigma_z\hat{z}$

$$
\sigma_x = \left(
    \begin{matrix}
        0 & 1 \\
        1 & 0
    \end{matrix}
\right)
$$

$$
\sigma_y = \left(
    \begin{matrix}
        0 & -i \\
        i & 0
    \end{matrix}
\right)
$$

$$
\sigma_z = \left(
    \begin{matrix}
        1 & 0 \\
        0 & -1
    \end{matrix}
\right)
$$

$$
\sigma_0 = \left(
    \begin{matrix}
        1 & 0 \\
        0 & 1
    \end{matrix}
\right)
$$

$$
H = \left(
    \begin{matrix}
        r_0 + r\cos\theta & re^{-i\phi}\sin\theta \\
        re^{i\phi}\sin\theta & r_0 - r\cos\theta
    \end{matrix}
\right)
$$

### Eigenvalues

$$\lambda_{1,2} = r_0 \pm r$$

### Eigenvectors

$$
\left(
    \begin{matrix}
    a \\ 
    b
    \end{matrix}
\right)
 = a|1\rangle + b|0\rangle  
$$

$$
|\lambda_1\rangle = 
\left(\begin{matrix}
    \cos\frac{\theta}{2}\\
    e^{i\phi}\sin\frac{\theta}{2}
\end{matrix}\right)
= \cos\frac{\theta}{2}|1\rangle + e^{i\phi}\sin\frac{\theta}{2}|0\rangle 
$$

$$
|\lambda_2\rangle =
\left(\begin{matrix}
    e^{i\phi}\sin\frac{\theta}{2}\\
    -\cos\frac{\theta}{2}
\end{matrix}\right)
= e^{i\phi}\sin\frac{\theta}{2}|1\rangle -\cos\frac{\theta}{2}|0\rangle
$$

### Eigenbasis

$$
\Lambda = 
\left(
    \begin{matrix}
    |\lambda_1\rangle & |\lambda_2\rangle
    \end{matrix}
\right)
=
\left(
    \begin{matrix}
    \langle 1| \lambda_1 \rangle & \langle 1|\lambda_2\rangle \\
    \langle 0 | \lambda_1 \rangle & \langle 0|\lambda_2\rangle
    \end{matrix}
\right)
=
\left(
    \begin{matrix}
    \cos\frac{\theta}{2} & e^{i\phi}\sin\frac{\theta}{2} \\
    e^{i\phi}\sin\frac{\theta}{2} & -\cos\frac{\theta}{2}
    \end{matrix}
\right)
$$

$$
\Lambda^{\dagger} = \left(
    \begin{matrix}
    \langle \lambda_1| 1 \rangle & \langle \lambda_1|0\rangle \\
    \langle \lambda_2 | 1 \rangle & \langle \lambda_2|0\rangle
    \end{matrix}
\right)
=
\left(
    \begin{matrix}
    \cos\frac{\theta}{2} & e^{-i\phi}\sin\frac{\theta}{2} \\
    e^{-i\phi}\sin\frac{\theta}{2} & -\cos\frac{\theta}{2}
    \end{matrix}
\right)
$$

$$
\det(\Lambda) = -e^{i\phi}\left(e^{-i\phi}\cos^2\frac{\theta}{2} + e^{i\phi}\sin^2\frac{\theta}{2}\right)
$$

### Time Evolution

$$
|\psi (t)\rangle = e^{-iHt}|\psi(0)\rangle = \sum_{k=1}^2 e^{i\lambda_k t}|\lambda_k\rangle\langle \lambda_k | \psi(0)\rangle =  \sum_{k=1}^2 c_k e^{i\lambda_k t}|\lambda_k\rangle
$$

$$
c_k = \langle\lambda_k|\psi(0)\rangle
$$

#### Transition Matrix

$$
P_{i\to f}(t) = |\langle f|e^{-iHt}|i\rangle|^2
$$
$$
= \left|c_{1_i}c_{1_f}e^{-i\lambda_1 t} + c_{2_i}c_{2_f}e^{-i\lambda_2 t}\right|^2
$$
$$
=|c_{1_i}|^2|c_{1_f}|^2 
+ |c_{2_i}|^2|c_{2_f}|^2 
+ c_{1_i}c_{1_f}c^*_{2_i}c^*_{2_f}e^{-i(\lambda_1 - \lambda_2)t} + \mathrm{h.c.}
$$

## General State Evolution

Starting with the initial state:

$$
|\psi(0)\rangle = |\theta_0,\phi_0\rangle = \cos\frac{\theta_0}{2}|1\rangle + e^{i\phi_0}\sin\frac{\theta_0}{2}|0\rangle
$$

The evolution of the state under the application of the general Hamiltonian $H = \vec{\sigma}\cdot\vec{r}$ will become:

$$
|\psi(t)\rangle = |\Theta(t), \Phi(t)\rangle = \cos\frac{\Theta(t)}{2}|1\rangle + e^{i\Phi(t)}\sin\frac{\Theta(t)}{2}|0\rangle
$$

Where $\Theta(t) = \Theta(\theta, \phi; \theta_0, \phi_0; t)$ and $\Phi(t) = \Phi(\theta,\phi;\theta_0,\phi_0; t)$ are functions of the:

- $\theta$: polar angle of $\vec{r}$
- $\phi$: azimuthal angle of $\vec{r}$
- $\theta_0$: initial state polar angle
- $\phi_0$: initial state azimuthal angle

The explicit expression is given by:

$$
\boxed{
\cos\frac{\Theta(t)}{2} 
= 
i\sin(rt)\sin(\theta)\sin\frac{\theta_0}{2}e^{i(\phi_0 - \phi)} 
+ \left[\cos(rt) - i\sin(rt)\cos(\theta)\right]\cos\frac{\theta_0}{2} 
}
$$

$$
\boxed{
e^{i\Phi(t)}\sin\frac{\Theta(t)}{2} 
= 
-e^{i\phi_0}\left[i\sin(rt)\sin(\theta)\cos\frac{\theta_0}{2}e^{-i(\phi_0 - \phi)} + \sin\frac{\theta_0}{2}\left[\cos(rt) + i\sin(rt)\cos\theta\right]\right]
}
$$

With these formula, we can take any input state, any Hamiltonian, and any time evolution duration, and compute the final state. 
**This is the general solution to all possible manipulations of a qubit in a pure state**.