# Adaptive Non-linear Intensity Modeling in Spatial Point Processes with GAMs

This repository accompanies the research on **using Generalized Additive Models (GAMs) to estimate intensity functions in Poisson and Cox point processes**. The work demonstrates how GAMs, with smoothing and basis functions, can capture non-linear dependencies in spatial data while avoiding overfitting through efficient cross-validation.

## 📌 Overview

Spatial point processes often exhibit **non-linear and complex intensity functions** that traditional linear models cannot capture.
This project introduces:

* Application of **Generalized Additive Models (GAMs)** to Poisson and Cox point processes.
* Efficient **cross-validation approach** for smoothing parameter selection.
* Use of **synthetic (Poisson, Cox) and real-world (gorilla nesting sites)** datasets to validate the method.
* GPU-accelerated implementation to reduce training time from **8 hours → 2 minutes**.

## ✨ Key Features

* **Flexible intensity modeling** with GAMs.
* Support for **homogeneous, inhomogeneous Poisson**, and **Cox processes**.
* **Basis functions (B-splines)** for non-parametric smooth estimation.
* **Cross-validation for smoothing parameter tuning**, avoiding computationally expensive likelihood maximization.
* Evaluation metrics: **MSE, R², log-likelihood, and integral differences**.
* **Ecological case study:** analysis of gorilla nesting sites with covariates (vegetation, heat, water proximity).

## 📊 Results Highlights

* **1D Poisson:** GAM explained \~95% of intensity variance (R² = 0.95).
* **2D Poisson:** MSE ≈ 38.6, R² ≈ 0.88.
* **2D Cox:** Captured clustering, optimal smoothing at \~1e-6.
* **Ecological data:** Revealed gorillas prefer **primary/secondary forests** and nest closer to water in dry seasons.

## 🔬 Applications

* **Ecology:** Modeling species distributions (gorilla nests, vegetation).
* **Biology:** Microscopy image analysis with unknown influencing factors.
* **Astronomy:** Modeling star distributions.
* **Hazards:** Earthquake or wildfire event intensity estimation.

## 📈 Future Work

* Implement **gradient descent optimization** for faster training.
* Extend to **multi-GAM ensembles** to capture localized variance/mean effects.
* Broader applications in **systems biology and climate studies**.

## 📚 References

* Wood, S. N. *Generalized Additive Models: An Introduction with R* (2006).
* Hastie, T., Tibshirani, R., Friedman, J. *The Elements of Statistical Learning* (2009).
* Youngman, B. D., Economou, T. (2017). *Generalised additive point process models for natural hazard occurrence*.
