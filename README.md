# The Thomson Problem

---

## Project Overview

This project addresses the **Thomson Problem**, a classic problem in physics and chemistry that seeks the **minimum-energy configuration of \( N \) electrons constrained to the surface of a unit sphere**. The electrons interact via a repulsive **Coulomb potential**, making the problem a rich example of nonlinear, many-body dynamics.

In this notebook, the problem is solved **numerically** by simulating the time evolution of the particles and identifying the configuration that minimizes the total electrostatic potential energy.

---

## Objectives

- Simulate the electrostatic interactions between \( N \) point charges confined to a spherical surface.
- Implement a numerical integration scheme (**Symplectic Euler method**) to solve the equations of motion.
- Visualize the evolution of the particle distribution and the resulting stable (minimum-energy) configuration.

---

## Methodology

The simulation follows these key steps:

- **Coulomb Potential**  
  Computes repulsive forces between all pairs of electrons using the \( 1/r \) interaction.

- **Surface Constraint**  
  After each time step, particle position vectors are re-normalized to ensure they remain on the surface of the unit sphere  
  \(
  |\mathbf{R}| = 1
  \)

- **Symplectic Euler Method**  
  A structure-preserving numerical integration scheme used to update velocities and positions while maintaining the Hamiltonian properties of the system.

- **Animation**  
  Uses `matplotlib.animation.FuncAnimation` to visualize how the electrons redistribute over time from an initially random configuration toward a minimum-energy state.

---

## Requirements

To run this notebook, the following Python libraries are required:

- `numpy` — numerical computations and linear algebra  
- `matplotlib` — 3D visualization and animation  
- `tqdm` — progress bar for simulation steps  

---

## Contents

- **Initial Setup**  
  Importing required libraries and defining physical constants.

- **Force Calculation**  
  Functions to compute the net Coulomb force acting on each electron.

- **Simulation Loop**  
  Implementation of the Symplectic Euler integration scheme.

- **Visualization**  
  - 3D scatter plots of the final electron configuration  
  - An animated sequence showing the evolution from a random initial state to a minimum-energy configuration

---

## Usage

1. Open the notebook in a Jupyter environment or Google Colab.
2. Run the cells sequentially to initialize the particles and parameters.
3. The simulation runs for a specified number of frames.
4. The final output includes:
   - A 3D visualization of electrons on the sphere  
   - An animation saved as a `.mp4` or `.gif` file (depending on available writers)

---

