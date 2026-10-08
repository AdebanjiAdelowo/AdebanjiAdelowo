# Adebanji Adelowo

**Applied Mathematician · Scientific Machine Learning Researcher**

I develop numerical methods for partial differential equations, fluid dynamics, inverse problems, reduced-order modelling, and data assimilation. My work combines mathematical analysis, numerical simulation, and scientific machine learning, with an emphasis on verification, reproducibility, and understanding where computational models succeed or fail.

[Website](https://adebanjioluwatimileyin.github.io/) · [CV](https://adebanjioluwatimileyin.github.io/cv.pdf) · [LinkedIn](https://linkedin.com/in/adebanjioluwatimileyin) · [Email](mailto:adelowooluwatimileyin@gmail.com)

## Research focus

**Numerical PDEs & scientific computing · Computational fluid dynamics · Inverse problems & uncertainty · Reduced-order modelling · Scientific machine learning · Data assimilation**

## Selected research projects

### FEM simulation of flow around a cylinder

A finite-element implementation of the Schäfer–Türek incompressible-flow benchmark using Taylor–Hood elements and Newton iteration. The project includes manufactured-solution verification, geometry and force-evaluation studies, and steady and periodic benchmark cases. The periodic study recovers vortex shedding with Strouhal number approximately **0.302**, while documenting the remaining sensitivity of force extrema to discretisation and post-processing choices.

[Code](https://github.com/AdebanjiAdelowo/fem-cylinder-flow) · [Case study](https://adebanjioluwatimileyin.github.io/projects/fem-cylinder-flow.html)

### Photoacoustic reconstruction

A sparse-view photoacoustic inverse-problem study comparing model-based and learned reconstruction methods. The project includes an explicit forward operator and adjoint, Tikhonov regularisation, learned reconstruction, and an unrolled model with exact data-consistency steps. Experiments also examine distribution shift, where thin vessel-like structures expose limitations of learned image priors.

[Code](https://github.com/AdebanjiAdelowo/photoacoustic-reconstruction) · [Case study](https://adebanjioluwatimileyin.github.io/projects/photoacoustic-reconstruction.html)

### Reduced-order modelling and operator learning for Burgers' equation

A comparative study of full-order simulation, POD–Galerkin reduction, DEIM hyper-reduction, and Fourier Neural Operators for the viscous Burgers equation. The project separates projection error, reduced-dynamics error, hyper-reduction error, and learned-operator generalisation, and includes reproducible CPU, Apple-silicon, and CUDA experiments.

[Code](https://github.com/AdebanjiAdelowo/neural-surrogate-burgers) · [Case study](https://adebanjioluwatimileyin.github.io/projects/neural-surrogate-burgers.html)

### Ensemble Kalman data assimilation for Lorenz–96

An Ensemble Kalman Filter study for the chaotic Lorenz–96 system, including covariance inflation, Gaspari–Cohn localisation, observation-density experiments, rank diagnostics, and repeated-seed studies. An independent linear-Gaussian Kalman experiment verifies the ensemble update, while small-ensemble experiments document genuine filter failure and under-dispersion rather than hiding unsuccessful regimes.

[Code](https://github.com/AdebanjiAdelowo/lorenz96-data-assimilation) · [Case study](https://adebanjioluwatimileyin.github.io/projects/lorenz96-data-assimilation.html)

## M.Sc. research

### Optimal mixing of passive scalars

My M.Sc. thesis in Mathematical Engineering studied mixing of passive scalars advected by incompressible flows under energy and enstrophy constraints. The computational work uses Fourier pseudo-spectral methods and an instantaneous optimisation strategy to investigate decay of negative-Sobolev mixing norms, together with resolution and convergence studies that distinguish empirical behaviour from theoretical bounds.

[Thesis repository](https://github.com/AdebanjiAdelowo/Master-Thesis) · [Research background](https://adebanjioluwatimileyin.github.io/research-outputs.html)

## Background and tools

- **M.Sc. Mathematical Engineering**, University of L’Aquila, Italy, 2021.
- **B.Sc. Mathematics**, Obafemi Awolowo University, Nigeria, 2018.

**Methods:** finite elements, spectral and pseudo-spectral methods, adjoint optimisation, Bayesian inference, POD–Galerkin reduction, DEIM, neural operators, ensemble data assimilation.

**Tools:** Python, NumPy, SciPy, PyTorch, FEniCSx, PETSc, scikit-learn, MATLAB, SQL, FastAPI, Docker, Git.

[Explore more projects and research →](https://adebanjioluwatimileyin.github.io/projects.html)

Based in L’Aquila, Italy. I welcome conversations about PhD research and collaborations in scientific computing, numerical PDEs, scientific machine learning, inverse problems, and computational modelling.
