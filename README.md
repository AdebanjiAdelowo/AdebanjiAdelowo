# Adebanji Adelowo

**Applied Mathematician · Machine Learning Engineer · Scientific Computing**

I'm a mathematician and machine learning engineer working across numerical methods, scientific computing, and applied AI. My research projects cover fluid dynamics, inverse problems, numerical PDEs, and data assimilation. In industry, I've worked on time-series analysis, anomaly detection, data pipelines, and machine learning services.

I care about more than whether a model produces a good result: I want to understand why it works, how reliably it performs, and where it breaks down.

[Website](https://adebanjiadelowo.github.io/) · [CV](https://adebanjiadelowo.github.io/cv.pdf) · [LinkedIn](https://linkedin.com/in/adebanjioluwatimileyin) · [Email](mailto:adelowooluwatimileyin@gmail.com)

## Research focus

Numerical PDEs · Computational fluid dynamics · Inverse problems · Reduced-order modelling · Scientific machine learning · Data assimilation

## Selected research projects

### Physics-informed neural operators for Darcy flow

I studied how the PDE-residual loss affects a Fourier Neural Operator trained on Darcy flow data, including a mismatch between the original example's residual and its dataset. With a corrected, data-consistent residual and the upstream 50-epoch training budget, the five-seed study reports **21.6% lower mean test relative L² error** than data-only training on Apple MPS; a pre-registered CUDA replication reports **21.5%**. These results apply to the tested dataset and training protocol, not to physics-informed models generally. A later regularisation comparison reused an examined test split and is not independent holdout confirmation.

[Code and experimental results](https://github.com/AdebanjiAdelowo/physicsnemo-pino-darcy) · [Scientific audit](https://github.com/AdebanjiAdelowo/physicsnemo-pino-darcy/blob/main/docs/SCIENTIFIC_AUDIT.md)

### Reduced-order modelling and operator learning for Burgers' equation

This project compares a pseudo-spectral solver, POD–Galerkin and DEIM reduced models, and learned surrogates for viscous Burgers' equation. I examine where the methods gain or lose accuracy and speed, including parameter extrapolation and the distinction between integration error and reduced-model error. For the tested solution family, classical reduced models remain accurate outside the training range while learned surrogates can deteriorate; the conclusions are specific to those experiments.

[Code](https://github.com/AdebanjiAdelowo/neural-surrogate-burgers) · [Case study](https://adebanjioluwatimileyin.github.io/projects/neural-surrogate-burgers.html)

### FEM simulation of flow around a cylinder

A finite-element study of the Schäfer–Türek incompressible-flow benchmark using Taylor–Hood elements and Newton iteration. It includes manufactured-solution checks, steady and periodic flow cases, and force-evaluation studies. The periodic case recovers vortex shedding with a Strouhal number of approximately **0.302**, while force extrema remain sensitive to discretisation and post-processing.

[Code](https://github.com/AdebanjiAdelowo/fem-cylinder-flow) · [Case study](https://adebanjioluwatimileyin.github.io/projects/fem-cylinder-flow.html)

### Photoacoustic reconstruction

I compare model-based and learned methods for sparse-view photoacoustic reconstruction, including an explicit forward operator and adjoint, Tikhonov regularisation, and an unrolled reconstruction model with data-consistency steps. Tests under distribution shift show how thin, vessel-like structures can challenge learned image priors.

[Code](https://github.com/AdebanjiAdelowo/photoacoustic-reconstruction) · [Case study](https://adebanjioluwatimileyin.github.io/projects/photoacoustic-reconstruction.html)

### Ensemble Kalman data assimilation for Lorenz–96

An Ensemble Kalman Filter study for the chaotic Lorenz–96 system. It explores covariance inflation, localisation, observation density, and ensemble size, with repeated-seed diagnostics and an independent linear-Gaussian update check. I also document filter failure and under-dispersion in small-ensemble settings rather than reporting only successful runs.

[Code](https://github.com/AdebanjiAdelowo/lorenz96-data-assimilation) · [Case study](https://adebanjioluwatimileyin.github.io/projects/lorenz96-data-assimilation.html)

## Applied ML and engineering

I've built machine learning and data-processing systems for aviation telemetry and connected devices. My work includes flight-phase classification, engine-RPM estimation, anomaly detection, transaction-log analysis, ETL pipelines, and API-backed tools. These projects have taught me to pay attention to data quality, validation, and the practical constraints of deploying models.

For research-specific evidence, limitations, and dated project assessments, see my [selected-projects scientific audit](https://github.com/AdebanjiAdelowo/selected-projects-scientific-audit).

## M.Sc. research

### Optimal mixing of passive scalars

My M.Sc. thesis in Mathematical Engineering studied mixing of passive scalars advected by incompressible flows under energy and enstrophy constraints. The computational work uses Fourier pseudo-spectral methods and an instantaneous optimisation strategy to investigate decay of negative-Sobolev mixing norms, together with resolution and convergence studies that distinguish empirical behaviour from theoretical bounds.

[Thesis repository](https://github.com/AdebanjiAdelowo/Master-Thesis) · [Research background](https://adebanjioluwatimileyin.github.io/research-outputs.html)

## Background and tools

- **M.Sc. Mathematical Engineering**, University of L’Aquila, Italy, 2021.
- **B.Sc. Mathematics**, Obafemi Awolowo University, Nigeria, 2018.

**Methods:** finite elements, spectral and pseudo-spectral methods, adjoint optimisation, Bayesian inference, POD–Galerkin reduction, DEIM, neural operators, ensemble data assimilation.

**Tools:** Python, NumPy, SciPy, PyTorch, FEniCSx, PETSc, scikit-learn, MATLAB, SQL, FastAPI, Docker, Git.

[Explore more projects and research](https://adebanjiadelowo.github.io/projects.html)

Based in Italy. I'm interested in research collaborations and engineering opportunities involving scientific computing, machine learning, numerical modelling, and applied AI.
