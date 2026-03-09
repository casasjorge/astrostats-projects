# Astrostats Projects

ASTR4303 (Astronomical Statistics) coursework — applications of statistical methods to real observational data, including Bayesian inference, MCMC sampling, time-series analysis, and regression.

## Project Structure

```
astrostats-projects/
├── 01-hubbles-law/
│   ├── 01_Hubbles_Law.ipynb
│   ├── data.dat
│   ├── Mann2015_Tables5_6_7.txt
│   └── README.md
├── 02-analysis/
│   ├── 02_Statistical_Analysis.ipynb
│   ├── data.dat
│   └── README.md
├── 03-light-curves/
│   ├── 03_Light_Curves.ipynb
│   ├── data.dat
│   └── README.md
├── 04-exoplanets/
│   ├── 04_Exoplanet_Detection.ipynb
│   ├── HARPS.dat
│   ├── HIRES.dat
│   └── README.md
└── 05-independent-project/
    ├── 05_Independent_Project_Galaxy_Rotation.ipynb
    ├── m33_data.dat
    ├── ngc2403_data.dat
    ├── ngc3198_data.dat
    ├── data_format.dat
    └── README.md
```

## Projects

### [01 — Hubble's Law](./01-hubbles-law)
Determines the Hubble constant H₀ from supernova SN1a distance-velocity data using weighted and unweighted linear regression. Includes bootstrap resampling for uncertainty estimation.

### [02 — Statistical Analysis](./02-analysis)
Applies MCMC sampling and corner plot visualization to multi-parameter astronomical datasets. Covers hypothesis testing, covariance analysis, and Bayesian model comparison.

### [03 — Light Curves](./03-light-curves)
Time-series analysis of photometric data. Uses Lomb-Scargle periodograms, rolling median filters, and MCMC to detect and characterize periodic signals and transient events.

### [04 — Exoplanet Detection](./04-exoplanets)
Fits Keplerian radial velocity models to HARPS and HIRES spectroscopic data using MCMC. Extracts orbital parameters and minimum planetary masses for multi-planet systems.

### [05 — Independent Project: Galaxy Rotation Curves](./05-independent-project)
Models rotation curves of M33, NGC 2403, and NGC 3198 using Freeman disk and NFW dark matter halo profiles. MCMC fitting constrains disk and halo mass parameters for each galaxy.

## Dependencies

```bash
pip install numpy scipy matplotlib pandas corner tqdm
```

## References

- Hubble (1929) — distance-velocity relation
- Freeman (1970) — exponential disk model
- Navarro, Frenk & White (1996) — NFW halo profile
- Mayor & Queloz (1995) — radial velocity exoplanet detection
- Foreman-Mackey et al. (2013) — emcee MCMC sampler

## ⚙️ Technical Notes

- All notebooks are compatible with Jupyter/IPython environments
- Plots are generated with `matplotlib` and displayed inline
- MCMC chains can require significant computation time for large datasets
- Corner plots are optimized for 2D-5D parameter spaces

## 🎯 Project Objectives

Each project demonstrates competency in:

- Statistical modeling of observational data
- Error analysis and uncertainty quantification
- Visualization of scientific results
- Parameter estimation using modern methods
- Interpretation of astronomical data

---

**Author:** Jorge  
**Course:** ASTR4303 - Astronomical Statistics  
**Last Updated:** 2026

For detailed information about each project, refer to the individual README files in each project directory.
