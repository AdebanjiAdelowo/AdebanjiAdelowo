# Adebanji Adelowo

**Applied Mathematician · Scientific Machine Learning Researcher**

I develop and verify numerical methods for PDEs, fluid dynamics, and inverse problems, with a focus on reduced-order modelling and scientific machine learning. My work combines mathematical analysis, reproducible simulation, and experience building machine-learning and data systems in industry.

[Website](https://adebanjioluwatimileyin.github.io/) · [Research](https://adebanjioluwatimileyin.github.io/research.html) · [Projects](https://adebanjioluwatimileyin.github.io/projects.html) · [CV](https://adebanjioluwatimileyin.github.io/cv.pdf) · [Email](mailto:adelowooluwatimileyin@gmail.com)

## Research themes

- **Numerical simulation:** spectral and finite-element methods for flow, transport, and mechanics, evaluated through exact solutions, convergence studies, and published benchmarks.
- **Inference and uncertainty:** adjoint-based PDE inversion, regularisation, Bayesian inference, topology optimisation, and ensemble data assimilation.
- **Scientific machine learning:** POD-Galerkin models, DEIM hyper-reduction, neural operators, and physics-informed networks, with attention to computational cost and generalisation beyond training data.

## Selected research

### Navier–Stokes and reduced-order modelling

I implemented a Fourier pseudo-spectral solver for two-dimensional incompressible flow, then extended it with tensorial POD-Galerkin and DEIM reduced models. At rank 16, the tensor ROM achieves **38.5× online speed-up at under 0.1% mean state error on its training trajectory**. The snapshot basis generalises poorly to unseen flow realisations, with approximately 99% error in the tested setting.

[Code](https://github.com/AdebanjiAdelowo/navier-stokes-2d) · [Case study](https://adebanjioluwatimileyin.github.io/projects/navier-stokes.html)

### Deterministic and Bayesian Darcy inversion

Adjoint-based optimisation and pCN MCMC recover a spatially varying permeability field from pressure observations. On a linear-Gaussian reference problem, the sampled posterior mean has **0.59% relative error against the analytical mean**. The nonlinear PDE posterior has limited mixing in several parameter dimensions; the small reference-problem error does not establish posterior accuracy for the full inverse problem.

[Code](https://github.com/AdebanjiAdelowo/darcy-inverse-problem) · [Case study](https://adebanjioluwatimileyin.github.io/projects/darcy.html)

### Finite elements and topology optimisation

A two-dimensional elasticity solver drives SIMP compliance minimisation under a material-volume constraint. Manufactured solutions test displacement convergence, and Taylor-remainder tests check compliance sensitivities. The canonical cantilever study demonstrates material redistribution and reduced compliance; quantitative mesh convergence remains a separate consideration.

[Code](https://github.com/AdebanjiAdelowo/fem-topology-optimization) · [Case study](https://adebanjioluwatimileyin.github.io/projects/topology-optimization.html)

## Further computational studies

| Project | Methods and findings |
|---|---|
| [Cylinder-flow benchmarks](https://github.com/AdebanjiAdelowo/fem-cylinder-flow) | Taylor–Hood FEniCSx/PETSc solver with manufactured-solution convergence checks and steady/unsteady cylinder-wake comparisons. Full unsteady benchmark reproduction is not claimed. |
| [Phase-field multiphase flow](https://github.com/AdebanjiAdelowo/boiling-phasefield-3d) | Coupled Allen–Cahn, Navier–Stokes, and heat transfer. A dedicated 1D Stefan solver reaches 0.079% interface-position error at Δx = 0.125 mm and t = 250 s, with matched densities. Numerical verification of the 3D solver does not establish physical boiling validation. |
| [Lorenz-96 data assimilation](https://github.com/AdebanjiAdelowo/lorenz96-data-assimilation) | Ensemble Kalman filtering with covariance localisation; over 11× RMSE reduction at the best tested radius relative to the unlocalised baseline. |
| [Burgers reduced models and neural operators](https://github.com/AdebanjiAdelowo/neural-surrogate-burgers) | A pseudo-spectral full-order solver compared with POD-Galerkin, DEIM, MLP, and FNO approximations. POD-ROM relative L² error is 0.152% in-distribution and 1.7% on the tested unseen initial-condition family. |
| [Advection–diffusion PINN](https://github.com/AdebanjiAdelowo/pinn-advection-diffusion) | A five-seed study of periodic boundary losses: derivative mismatch falls 7–38× with derivative enforcement, without reliable improvement in global solution accuracy at the original training budget. |
| [Photoacoustic reconstruction](https://github.com/AdebanjiAdelowo/photoacoustic-reconstruction) | Learned U-Net refinement improves PSNR by approximately 11.8 dB over time-reversal at 16 sensors on synthetic test phantoms; whole-image SSIM is lower because of residual background artefacts. |
| [Differentiable material recovery](https://github.com/AdebanjiAdelowo/diff-pbr) | Cook–Torrance inverse rendering in PyTorch. Six views are used for optimisation and two are held out: MSE is 1.82 × 10⁻⁶ on training views and 1.02 × 10⁻⁵ on held-out views. |
| [NeRF and TensoRF](https://github.com/AdebanjiAdelowo/nerf-tensorf) | From-scratch implementations: TensoRF reaches 16.7 dB PSNR versus 13.7 dB for NeRF on 40 held-out views, using half the training iterations. |
| [3D liver segmentation](https://github.com/AdebanjiAdelowo/abdominal-ct-segmentation) | A 3D U-Net reaches 0.9886 Dice on 26 centre-cropped, 128³ model-selection volumes. This is not an independent full-volume test result. |

## Engineering and applied ML

- **[Flight data monitoring at Intuos Srl](https://github.com/AdebanjiAdelowo/intuos-fdm-dashboard):** FastAPI, IBM DB2, React/Vite, and Docker support query-on-demand analysis of recorded flight telemetry. The flight-phase classifier achieves 0.999 weighted F1 in five-fold cross-validation; this is not a prospective deployment score.
- **[Aircraft engine audio monitor](https://github.com/AdebanjiAdelowo/aircraft-engine-monitor):** a personal Raspberry Pi/ESP32 prototype for FFT-based RPM estimation, tested on Tecnam P92 / Rotax 912 recordings. No tachometer ground truth was collected; the documented configuration has approximately 21% chunk-level order ambiguity and is not flight-safety validated.
- **[LLM systems and model compression](https://github.com/AdebanjiAdelowo/ai-projects-portfolio):** retrieval, structured data access, fine-tuning, and compression projects with differing implementation and evaluation coverage. The distilled FinBERT student achieves **96.91% accuracy and 0.9691 weighted F1** on a 453-sentence Financial PhraseBank test split, with 88.22M parameters.

Additional implementations include [TV image inpainting](https://github.com/AdebanjiAdelowo/Image_inpainting), [image denoising](https://github.com/AdebanjiAdelowo/Image_denoising_using_ResNet), [differentiable subsurface scattering](https://github.com/AdebanjiAdelowo/sss-dipole), and a [GPT-style language model](https://github.com/AdebanjiAdelowo/nano-gpt).

## Background

**M.Sc. Mathematical Engineering**, University of L’Aquila, Italy (2018–2021). Supervisor: Prof. Stefano Spirito.

Thesis: *Bounds on mixing of passive scalars advected by incompressible energy and enstrophy constrained flows and Anomalous dissipation*.

The accompanying [optimal-mixing implementation](https://github.com/AdebanjiAdelowo/Master-Thesis) derives the constrained optimal velocity and ports Gautam Iyer’s MATLAB scheme to a Python pseudo-spectral solver. The experiments show exponential H⁻¹ decay with resolution-dependent fitted mixing rates. A deterministic rerun matches the implementation’s own recorded outputs to four decimal places.

**B.Sc. Mathematics**, Obafemi Awolowo University, Nigeria (2014–2018).

Thesis: *Application of the Galerkin Finite Element Method to the One-Dimensional Stefan Problem*.

## Technical tools

**Scientific computing:** Python, NumPy, SciPy, MATLAB, FEniCSx, PETSc, FFT-based methods, LaTeX.

**Machine learning:** PyTorch, TensorFlow, scikit-learn, automatic differentiation.

**Software and data:** FastAPI, Docker, SQL, PostgreSQL, IBM DB2, React/Vite, Git.

## Connect

Based in L’Aquila, Italy. I am interested in research on uncertainty-aware PDE surrogates, reduced-order and inverse models, and data-efficient learning for physical systems.

[Website](https://adebanjioluwatimileyin.github.io/) · [LinkedIn](https://linkedin.com/in/adebanjioluwatimileyin) · [Email](mailto:adelowooluwatimileyin@gmail.com)
