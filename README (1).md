# Statistical Methods Project: Modeling Wrestler Scores

**Author:** Mobin Ghorbani  
**Course:** Statistical Methods  
**Topic:** Bayesian Modeling of Hassan Yazdani's Wrestling Scores  

## Project Overview

This project analyzes and models the average score of Hassan Yazdani (renowned Iranian wrestler) in international matches from 2015 to 2022 using both **frequentist** and **Bayesian** statistical approaches.

## Objective

Develop a comprehensive statistical model culminating in a Gibbs-sampling mixture model that captures latent "fitness" states (well-prepared vs. not well-prepared) in Hassan Yazdani's wrestling performance.

## Key Analyses

### 1. **Frequentist Estimates** (Step 1)
- Calculate sample mean (μ̂) and variance (σ̂²) from 2015-2021 data (n=58)
- Results: μ̂ ≈ 9.40, σ̂² ≈ 7.72
- Prior-predictive distributions for uncertainty quantification

### 2. **Bayesian Update** (Step 2)
- Update beliefs with 2022 data (7 new match scores)
- Posterior mean: μ ≈ 9.55
- Posterior variance: σ² ≈ 1.04

### 3. **Mixture Model** (Step 3)
- Two latent fitness states: **Well-prepared** (Z=1) and **Not well-prepared** (Z=0)
- Empirical priors from top 10% of historical scores
- Gibbs sampling for joint posterior inference

## Technologies & Libraries

- **Python 3.x**
- **NumPy** - numerical computations
- **Matplotlib & Seaborn** - visualization
- **SciPy** - statistical distributions

## Project Structure

```
SmProject/
├── SmProject.ipynb          # Main analysis notebook
├── requirements.txt         # Python dependencies
├── .gitignore              # Git ignore file
├── README.md               # This file
└── LICENSE                 # MIT License (optional)
```

## Installation & Setup

1. **Clone the repository:**
   ```bash
   git clone https://github.com/YOUR_USERNAME/statistical-methods-wrestling.git
   cd statistical-methods-wrestling
   ```

2. **Create a virtual environment:**
   ```bash
   python -m venv venv
   source venv/bin/activate  # On Windows: venv\Scripts\activate
   ```

3. **Install dependencies:**
   ```bash
   pip install -r requirements.txt
   ```

4. **Run the notebook:**
   ```bash
   jupyter notebook SmProject.ipynb
   ```

## Data

- **Historical Data:** Hassan Yazdani's match scores from 2015–2021 (58 observations)
- **New Data:** 7 additional scores from 2022
- **Format:** Stored directly in notebook as NumPy arrays

## Key Findings

- **Mean Score Stability:** Posterior estimates remain centered around 9.5 points
- **Variance Reduction:** Bayesian update significantly reduces uncertainty
- **Fitness States:** Clear distinction between high-performance (θ₁) and baseline states
- **Model Convergence:** Gibbs sampler shows good mixing and convergence diagnostics

## How to Use This Project

1. Open `SmProject.ipynb` in Jupyter Notebook or JupyterLab
2. Run cells sequentially to reproduce all analyses
3. Modify priors or data as needed for extended analyses
4. Review visualizations (histograms, posteriors, trace plots) for model diagnostics

## Results Reproducibility

All results are **fully reproducible** with:
- Fixed random seed (RNG seed = 42)
- Exact data specifications in notebook
- Clear hyperparameter documentation

## Future Enhancements

- [ ] Add time-series analysis for temporal trends
- [ ] Extend mixture model to 3+ latent states
- [ ] Incorporate external features (opponent strength, venue, etc.)
- [ ] Bayesian model comparison (LOO-CV, WAIC)

## References

- Gelman, A., et al. (2013). *Bayesian Data Analysis* (3rd ed.)
- Probabilistic Programming concepts applied to athletic performance modeling

## License

This project is licensed under the **MIT License** – see LICENSE file for details.

## Contact

For questions or feedback, please reach out:
- **Email:** mobin.ghorbani@example.com
- **GitHub:** [@MobinGhorbani](https://github.com/MobinGhorbani)

---

**Last Updated:** November 2025  
**Status:** Complete & Ready for Publication
