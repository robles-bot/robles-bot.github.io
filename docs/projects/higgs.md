# Higgs Mass Reconstruction

**Course:** PHYS 152 - Machine Learning in Physics
**Institution:** UC Santa Cruz
**Term:** Winter 2024

[Download Notebook](higgs-mass-reconstruction.ipynb){ .md-button }

---

## Overview

A neural network regression model to reconstruct the invariant mass of the Higgs boson from simulated H→μ⁺μ⁻ decay events. The model learns the non-linear relationship between collider coordinates and particle mass.

## Physics Background

### Relativistic Kinematics

The four-momentum vector is defined as:

$$
\mathbf{p}^{\mu} = \left(\frac{E}{c}, \mathbf{p} \right)
$$

The invariant mass of a parent particle can be reconstructed from its decay products using:

$$
m = \sqrt{2p_{T1}p_{T2}\left[\cosh(\eta_1-\eta_2)-\cos(\phi_1-\phi_2)\right]}
$$

### Collider Coordinates

- **Transverse momentum** ($p_T$): Momentum perpendicular to the beam axis
- **Pseudorapidity** ($\eta$): $\eta = -\ln\left(\tan\frac{\theta}{2}\right)$
- **Azimuthal angle** ($\phi$): Angle in the transverse plane

## Model Architecture

A fully-connected neural network with 9 layers:

```
Input (35 features)
    → Linear(35, 100) → Tanh
    → Linear(100, 75) → Tanh
    → Linear(75, 60)  → Tanh
    → Linear(60, 50)  → Tanh
    → Linear(50, 40)  → Tanh
    → Linear(40, 30)  → Tanh
    → Linear(30, 20)  → Tanh
    → Linear(20, 10)  → Tanh
    → Linear(10, 1)   → Sigmoid
Output (invariant mass)
```

## Training

| Parameter     | Value   |
|---------------|---------|
| Learning Rate | 0.01    |
| Momentum      | 0.2     |
| Epochs        | 1000    |
| Batch Size    | 49,999  |
| Test Size     | 10,000  |
| Loss Function | MSE     |
| Optimizer     | SGD     |

## Input Features

35 features from simulated collider data:

- Number of jets, leptons, b-tagged jets
- Missing transverse energy (MET)
- Lepton kinematics ($p_T$, $\eta$, $\phi$) for 2 leptons
- Jet kinematics ($p_T$, $\eta$, $\phi$, b-tag) for up to 6 jets

## Results

The model successfully learns to predict the Higgs boson mass (~125 GeV) from low-level collider features, demonstrating that the neural network has effectively learned:

- Relativistic kinematics
- Collider coordinate transformations
- The non-linear relationship between detector observables and invariant mass

## Tools

- PyTorch
- scikit-learn (preprocessing, train/test split)
- h5py (HDF5 data loading)
- pandas, NumPy, Matplotlib
