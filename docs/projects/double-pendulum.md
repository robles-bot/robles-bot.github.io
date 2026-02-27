# Double Pendulum Dynamics

**Course:** PHYS 115 - Computational Physics
**Institution:** UC Santa Cruz
**Term:** Fall 2023

[Download Notebook](double-pendulum.ipynb){ .md-button }

---

## Overview

A numerical exploration of double pendulum dynamics using the Runge-Kutta 4 method. The project progresses from single pendulum analysis to the chaotic behavior of coupled pendulums, including normal mode analysis.

## Methods

### Lagrangian Mechanics

The equations of motion are derived from the Lagrangian:

$$
\mathcal{L} = \frac{1}{2}(m_1+m_2)l_1^{2}\dot{\theta}^{2}_{1} + \frac{1}{2}m_2l_2^{2}\dot{\theta}^{2}_{2} + m_2l_1l_2\dot{\theta}_{1}\dot{\theta}_{2}\cos(\theta_{1}-\theta_{2}) + (m_1+m_2)gl_1\cos(\theta_1) + m_2gl_2\cos(\theta_{2})
$$

Applying the Euler-Lagrange equations yields a coupled system of second-order ODEs.

### Runge-Kutta 4 Integration

The system is solved numerically using RK4 with the state vector:

$$
\vec{x} = \begin{bmatrix} \theta_1 \\ \omega_1 \\ \theta_2 \\ \omega_2 \end{bmatrix}
$$

## Cases Explored

| Case | Approximation | Damping | Driving Force |
|------|---------------|---------|---------------|
| 1a   | Small angle   | No      | No            |
| 1b   | None          | No      | No            |
| 2a   | Small angle   | Yes     | Yes           |
| 2b   | None          | Yes     | Yes           |

## Key Results

- **Energy Conservation:** Phase plots show closed orbits for undamped systems, confirming energy conservation
- **Damping Effects:** Systems spiral toward attractors as energy dissipates
- **Normal Modes:** Eigenvalue analysis of the linearized system reveals normal mode frequencies
- **Chaos:** Small differences in initial conditions lead to dramatically different trajectories

## Normal Mode Analysis

The linearized system can be written as an eigenvalue problem:

$$
\begin{bmatrix}
(m_1+m_2)l_1^2 & m_2l_1l_2 \\
m_2l_1l_2 & m_2l_2^2
\end{bmatrix}
\begin{bmatrix}
\ddot{\theta}_1 \\
\ddot{\theta}_2
\end{bmatrix}
= -\omega^2
\begin{bmatrix}
\theta_1 \\
\theta_2
\end{bmatrix}
$$

The eigenvalues give the normal mode frequencies, which produce stable oscillatory behavior when used as initial conditions.

## Tools

- Python, NumPy, Matplotlib
- Custom `singlePendulum` and `doublePendulum` classes implementing RK4
