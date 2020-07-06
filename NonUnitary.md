# Non Unitary Evolution of a Qubit

[Reference](https://www.arxiv-vanity.com/papers/cond-mat/0108339/)

The non-unitary evolution occurs when a qubit is coupled to an environment.

The **Bloch equations** describe phenomenologically the evolution of a density matrix $\rho$ for a qubit coupled to an environment, while under the typical electromagnetic Hamiltonian.

$$
\vec{M} = \mathrm{Tr}(\rho\vec{\sigma})
$$

$$
\dot{M_x} = -\frac{1}{T_2}M_x - \delta M_y\\
\dot{M_y} = -\frac{1}{T_2}M_y + \delta M_x + R_0 M_z\\
\dot{M_z} = -\frac{1}{T_1}(M_z + 1) - R_0M_y
$$

$T_1$ is called the depolarizing time. Terms that are also associated to this are:

- inelastic spin-flip
- spin-lattice relaxation

$T_2$ is called the dephasing time, as it describes the transverse relaxation. Also called spin-spin relaxation time.

In the case we are describing an ensemble of qubits, there will be a different constant $T_2^* \leq T_2$ that accounts for the inhomogeneous Zeeman splitting of the qubits.

## Spin Echo

Spin echo is the revival of the magnetization vector (excepting depolarization) following an application of a sequence of electromagnetic pulses that reverses the inhomogeneous dephasing process. 
Sometimes called Hahn echoes by the first scientist to notice the effect.
This is used to measure the spin-spin relaxation time $T_2$ instead of the ensemble average $T_2^*$.