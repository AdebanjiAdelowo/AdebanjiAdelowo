# Adebanji Adelowo

**Mathematical Engineer · Scientific Machine Learning · Computational PDEs**

I work at the intersection of applied mathematics, numerical simulation, and machine learning. My background is in PDE analysis and scientific computing (pseudo-spectral methods, finite elements, FFT-based solvers), and I build on it with data-driven methods: physics-informed neural networks, reduced-order models, and learned reconstruction for inverse problems. I am interested in physical systems where the mathematical structure of the problem, not just the data, should shape the model.

## Research Interests

Computational PDEs · Scientific Machine Learning · Inverse Problems · Reduced-Order Modelling · Physics-Informed ML · Computational Imaging · Numerical Optimisation

## Featured Research & Projects

### Optimal Mixing of Passive Scalars
[Master-Thesis](https://github.com/AdebanjiAdelowo/Master-Thesis)

M.Sc. thesis deriving the Lin-Thiffeault-Doering optimal-mixing velocity field for a passive scalar advected by an enstrophy-constrained incompressible flow, via a constrained-optimisation argument. Implemented as a pseudo-spectral solver in Python (Leray projection, RK45 time-stepping), ported from Gautam Iyer's MATLAB code. Confirms the predicted exponential H⁻¹ decay and reproduces the reference implementation's mixing-rate output to four decimal places, with a resolution-sensitivity study (N=32 vs. N=64) showing the fitted decay exponent is itself resolution-dependent.

### Phase-Field Modelling of Boiling Flows
[boiling-phasefield-3d](https://github.com/AdebanjiAdelowo/boiling-phasefield-3d)

A conservative Allen-Cahn phase-field model for vapour-liquid phase change, coupled to incompressible Navier-Stokes and an energy equation with a latent-heat source term. The pressure Poisson equation has constant coefficients by construction and is solved directly with FFTs, a property that carries over unchanged to 3D. The 2D bubble-growth benchmark agrees with the analytical growth rate, with the error decreasing under grid refinement. A dedicated non-periodic 1D Stefan solver, developed after diagnosing the original benchmark implementation, converges at first order to 0.079% interface-position error (Δx = 0.125 mm, t = 250 s) with verified mass and energy balances. The 3D solver is numerically verified, not physically validated; the general multiphase heat-flux pathway remains under validation.

### Reduced-Order and Neural Surrogate Modelling of Burgers' Equation
[neural-surrogate-burgers](https://github.com/AdebanjiAdelowo/neural-surrogate-burgers)

Compares a POD-Galerkin reduced-order model against a neural-network (MLP) surrogate for the viscous Burgers' equation, both checked against a from-scratch finite-difference solver validated for mass conservation and grid convergence. In-distribution, the POD-ROM reaches 0.15% relative L2 error versus 0.79% for the surrogate; out-of-distribution, the surrogate's error grows to about 56% while the ROM stays near 0.06%, a deliberately reported negative result rather than a cherry-picked one.

### Physics-Informed Neural Network: 1D Advection-Diffusion
[pinn-advection-diffusion](https://github.com/AdebanjiAdelowo/pinn-advection-diffusion)

A PyTorch PINN that learns the solution of the 1D advection-diffusion equation by enforcing the PDE residual, initial condition, and periodic boundary condition through automatic differentiation, with no labelled interior data. Reaches 5.1×10⁻³ relative L2 error against the closed-form analytical solution.

### Learned Photoacoustic Image Reconstruction
[photoacoustic-reconstruction](https://github.com/AdebanjiAdelowo/photoacoustic-reconstruction)

A photoacoustic tomography pipeline built around a pseudo-spectral acoustic-wave forward model (j-Wave), generating sensor data from sparse transducer arrays. Reconstruction combines a classical time-reversal baseline with a learned U-Net refinement stage. On the project's sparse-array test set, the learned stage improves PSNR from 18.97 dB (time-reversal) to 30.73 dB, alongside an explicit investigation of a PSNR/SSIM disagreement caused by background artefacts in the learned output. Scoped as a validated MVP on one synthetic dataset, not a general-purpose reconstruction method.

### Differentiable Inverse Rendering
[diff-pbr](https://github.com/AdebanjiAdelowo/diff-pbr)

A differentiable Cook-Torrance renderer (GGX normal distribution, Schlick Fresnel, Smith geometry term) written in pure PyTorch and NumPy, with no external differentiable-rasterisation library. Recovers per-texel albedo, normal, roughness, and metallic maps from 8 multi-view synthetic photographs by gradient descent through the shading model, converging MSE from about 1×10⁻⁵ to 1×10⁻⁶ over 2,000 steps.

### 3D Liver Segmentation from Abdominal CT
[abdominal-ct-segmentation](https://github.com/AdebanjiAdelowo/abdominal-ct-segmentation)

A 3D U-Net trained end-to-end for binary liver segmentation on the Medical Segmentation Decathlon (Task03) dataset, 131 CT volumes, using foreground-biased patch sampling, a combined soft-Dice and BCE loss, cosine learning-rate annealing, and Gaussian sliding-window inference. 0.9886 Dice on the 26-volume 128³ centre-cropped validation split used for model selection, after 200 epochs on a single Kaggle T4 GPU. A leakage-controlled full-volume evaluation pipeline with physical-unit HD95 has been implemented; independent evaluation is pending retraining on the original NIfTI data.

## Selected Results

| Project | Result |
|---|---|
| Optimal mixing (Master-Thesis) | Reproduces reference exponential H⁻¹ decay; resolution study at N=32 and N=64 |
| Phase-field boiling, 2D bubble growth | Matches analytical growth rate; error decreases under grid refinement |
| Phase-field boiling, dedicated 1D Stefan solver | First-order convergence; 0.079% interface-position error at Δx = 0.125 mm (t = 250 s) |
| Burgers ROM vs. surrogate | 0.15% vs. 0.79% relative L2 error in-distribution; 0.06% vs. 56% out-of-distribution |
| PINN, advection-diffusion | 5.1×10⁻³ relative L2 error vs. analytical solution |
| Photoacoustic reconstruction | PSNR 18.97 dB (time-reversal) → 30.73 dB (learned refinement) |
| Differentiable inverse rendering | MSE converges from ~1×10⁻⁵ to ~1×10⁻⁶ over 2,000 steps |
| Liver segmentation (3D U-Net) | 0.9886 Dice on the 26-volume 128³ centre-cropped validation split used for model selection |

All numbers above are read directly from each project's own logged output, saved metrics, or notebook results, not aspirational figures.

## Additional Work

- [sss-dipole](https://github.com/AdebanjiAdelowo/sss-dipole): differentiable multi-layer dipole BSSRDF (Donner and Jensen 2005) in PyTorch, parameterised for six Fitzpatrick skin types.
- [nerf-tensorf](https://github.com/AdebanjiAdelowo/nerf-tensorf): vanilla NeRF and TensoRF (Chen et al. 2022) implemented from scratch and compared on a synthetic scene (TensoRF: 17.5 dB PSNR / 0.83 SSIM in half the training iterations of NeRF).
- [Image_inpainting](https://github.com/AdebanjiAdelowo/Image_inpainting): TV-regularised image restoration via preconditioned Douglas-Rachford splitting on the dual saddle-point problem.
- [Image_denoising_using_ResNet](https://github.com/AdebanjiAdelowo/Image_denoising_using_ResNet): residual channel-attention blocks for blind greyscale denoising, 33.7 dB PSNR versus a 28.3 dB plain-ResNet baseline.
- [aircraft-engine-monitor](https://github.com/AdebanjiAdelowo/aircraft-engine-monitor): FFT-based engine RPM estimation from microphone audio on a Raspberry Pi, streamed to an ESP32 over UART.
- [intuos-fdm-dashboard](https://github.com/AdebanjiAdelowo/intuos-fdm-dashboard): full-stack flight-telemetry analytics platform (FastAPI, IBM DB2, React/Vite) serving Random Forest and LightGBM flight-phase classifiers in production.
- [ai-projects-portfolio](https://github.com/AdebanjiAdelowo/ai-projects-portfolio): applied LLM systems including a RAG assistant, a two-stage NL-to-SQL pipeline, and a FinBERT compression pipeline (pruning plus distillation) reaching 96.9% accuracy/F1 at 88M parameters, close to the 110M-parameter baseline's 97.6%/0.976.
- [nano-gpt](https://github.com/AdebanjiAdelowo/nano-gpt): a GPT-style transformer built from scratch in PyTorch, trained character-level on Tiny Shakespeare.

## Technical Stack

**Scientific Computing:** Python, NumPy, SciPy, MATLAB, pseudo-spectral methods, finite elements, FFT-based PDE solvers

**Machine Learning:** PyTorch, TensorFlow/Keras, scikit-learn, MONAI, automatic differentiation

**Numerical Methods:** POD-Galerkin reduced-order models, physics-informed neural networks, variational (TV) regularisation, Douglas-Rachford splitting

**Backend / Data:** FastAPI, Docker, PostgreSQL, IBM DB2, React/Vite

**Tools:** Git, LaTeX

## Current Research Direction

I am interested in combining PDE-based mathematical models, numerical simulation, and machine learning to build surrogate, reduced-order, and inverse models for physical systems, from multiphase flow and reduced-order fluid models to learned reconstruction for computational imaging. A recurring theme in this work is being explicit about where a data-driven surrogate agrees with the physics it approximates, and where it does not.

## Background

**M.Sc. Mathematical Engineering**, University of L'Aquila, Italy (2018-2021)
Thesis: Lower Bounds on the Mix Norm of Passive Scalars Advected by Incompressible Enstrophy-Constrained Flows

**B.Sc. Mathematics**, Obafemi Awolowo University, Nigeria (2014-2018)
Thesis: Application of the Galerkin Finite Element Method to the One-Dimensional Stefan Problem

## Connect

- Website: [adebanjioluwatimileyin.github.io](https://adebanjioluwatimileyin.github.io)
- LinkedIn: [linkedin.com/in/adebanjioluwatimileyin](https://linkedin.com/in/adebanjioluwatimileyin)
- Email: adelowooluwatimileyin@gmail.com
