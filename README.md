# Pipe Flow Development Length Simulation using ANSYS Fluent and CFX

## Overview

This project presents a computational fluid dynamics (CFD) analysis of laminar flow development inside a circular pipe using **ANSYS Fluent** and **ANSYS CFX**.

The objective of this study is to investigate the hydrodynamic development length in internal pipe flow and analyze how Reynolds number affects the velocity distribution and entrance region behavior.

The project includes:

* Theoretical analysis of Hagen–Poiseuille flow
* CFD simulation of laminar incompressible flow
* Parametric study for multiple Reynolds numbers
* Velocity profile analysis
* Development length estimation
* Comparison between Fluent and CFX results
* Validation using analytical relations

---

## Background

Laminar incompressible flow inside a circular pipe is commonly known as **Hagen–Poiseuille flow**.

As fluid enters a pipe with a uniform inlet velocity profile, boundary layers develop near the walls due to viscous effects. These layers gradually grow and merge until the velocity profile becomes fully developed and parabolic.

The entrance length for laminar pipe flow can be estimated using:

```text
L = 0.065 × Re × D
```

Where:

* `L` = hydrodynamic development length
* `Re` = Reynolds number
* `D` = pipe diameter

---

## Objectives

The main goals of this project are:

* Simulate laminar flow inside a circular pipe
* Investigate the effect of Reynolds number on development length
* Observe the formation of the fully developed parabolic velocity profile
* Compare analytical and numerical results
* Compare Fluent and CFX simulations

---

## Software Used

* ANSYS Fluent
* ANSYS CFX
* ANSYS Meshing
* ANSYS DesignModeler

---

## Geometry

A circular pipe with:

* Length = 3 m
* Radius = 0.1 m

was modeled for the simulations.

### Geometry

![Pipe Geometry](images/geometry/pipe-geometry.png)

---

## Mesh Generation

A structured mesh was generated for the pipe domain to ensure stable and accurate numerical results.

### Pipe Mesh

![Pipe Mesh](images/mesh/pipe-mesh.png)

### Mesh Details

![Mesh Details](images/mesh/mesh-details.png)

---

## Boundary Conditions

The following conditions were applied:

* Inlet velocity = 1 m/s
* Outlet gauge pressure = 0 Pa
* No-slip condition at pipe walls
* Steady laminar incompressible flow

---

## Reynolds Numbers Studied

Different Reynolds numbers were obtained by changing the dynamic viscosity.

| Reynolds Number | Dynamic Viscosity (kg/m·s) |
| --------------- | -------------------------- |
| 100             | 0.002                      |
| 150             | 0.00133                    |
| 200             | 0.001                      |

---

## Development Length Estimation

The analytical development lengths were calculated using:

```text
L = 0.065 × Re × D
```

| Reynolds Number | Development Length (m) |
| --------------- | ---------------------- |
| 100             | 1.3                    |
| 150             | 1.95                   |
| 200             | 2.6                    |

---

# Results

## Axial Velocity Development

The velocity profile develops gradually from a uniform inlet profile to a fully developed parabolic profile.

![Velocity Development](images/results/velocity-development-re100-re150-re200.png)

---

## Radial Velocity Distribution

The fully developed velocity distribution inside the pipe follows the expected parabolic behavior predicted by Hagen–Poiseuille theory.

![Radial Velocity Profile](images/results/radial-velocity-profile-re100-re150-re200.png)

---

## Fluent vs CFX Comparison

The problem was also solved using ANSYS CFX for Reynolds number 100.

The comparison between Fluent and CFX showed good agreement in predicting axial velocity development.

![Fluent vs CFX](images/cfx-comparison/fluent-vs-cfx-re100.png)

---

## Key Observations

* Development length increases with increasing Reynolds number.
* The fully developed region occurs farther downstream for larger Reynolds numbers.
* Velocity becomes parabolic in the fully developed region.
* Maximum velocity occurs at the pipe centerline.
* Maximum velocity is approximately twice the average velocity.
* Fluent and CFX produced closely matching results.
* CFX showed slightly faster convergence behavior.

---

## Theoretical Concepts

This project is based on:

* Navier–Stokes equations
* Continuity equation
* Hagen–Poiseuille flow theory
* Laminar internal flow analysis
* Hydrodynamic entrance length

---

## Repository Structure

```text
pipe-flow-development-length-ansys/
│
├── README.md
│
├── report/
│   └── pipe-flow-development-length-report.pdf
│
├── images/
│   ├── geometry/
│   ├── mesh/
│   ├── results/
│   └── cfx-comparison/
│
├── data/
│
└── fluent-setup/
    └── simulation-notes.md
```

---

## References

1. Frank M. White — Fluid Mechanics
2. ANSYS Fluent Documentation
3. ANSYS CFX Documentation

---

## Author

**Ali Darfashi**
Mechanical Engineering Student
Computational Fluid Dynamics (CFD) Enthusiast
