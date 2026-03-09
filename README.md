# Astrostats Projects Repository

A comprehensive collection of astronomy and statistical analysis projects completed for ASTR4303 (Astronomical Statistics) and related studies. This repository showcases applications of statistical methods to astronomical data analysis, including exoplanet detection, galaxy dynamics, cosmological measurements, and transient phenomena analysis.

## 📁 Project Structure

This repository contains five major projects, each focusing on different aspects of astronomical data analysis:

### [01 - Independent Project: Galaxy Rotation Curves](./01-independent-project)
**Modeling Dark Matter Using Galaxy Rotation Curves**

A comprehensive analysis of galaxy rotation curves using both baryonic matter models and dark matter halo profiles. This project fits observational data from galaxies (M33, NGC 2403, NGC 3198) to Freeman (1970) disk models and Navarro-Frenk-White (NFW) dark matter halo profiles using Monte Carlo Markov Chain (MCMC) methods.

**Key Topics:**
- Galaxy rotation curve fitting
- Freeman exponential disk model
- NFW dark matter halo model
- Bayesian inference and MCMC parameter estimation
- Error analysis and model comparison

**Key Outputs:** 
- Fitted disk and halo parameters
- Mass distributions
- Corner plots (parameter correlations)
- Model residuals and goodness-of-fit analysis

---

### [02 - Lab 1: Hubble's Law and the Hubble Constant](./02-lab1-hubbles-law)
**Measuring Cosmic Expansion Using Supernova Data**

This lab implements linear regression techniques to determine the Hubble constant from supernova (SN1a) observations. Students use velocity-distance data to establish the relationship between cosmic expansion and recession velocity, a fundamental measurement in cosmology.

**Key Topics:**
- Linear regression (both weighted and unweighted)
- Hubble's Law and cosmic expansion
- Error propagation and uncertainty quantification
- Residual analysis and model diagnostics
- Statistical significance testing

**Key Outputs:**
- Hubble constant estimate with confidence intervals
- Regression plots with error bars
- Residual plots for model validation
- Statistical summary tables

---

### [03 - Lab 2: Advanced Statistical Analysis](./03-lab2-analysis)
**Statistical Methods and Data Validation**

A laboratory focused on testing advanced statistical techniques including corner plots for parameter space exploration, correlation analysis, and hypothesis testing. This project serves as a bridge between basic statistics and complex Bayesian inference methods.

**Key Topics:**
- Parameter space visualization
- Correlation matrices and covariance analysis
- Statistical hypothesis testing
- Data validation and quality checks
- Distribution fitting and goodness-of-fit tests

**Key Outputs:**
- Corner plots and covariance matrices
- Statistical summaries and distributions
- Test results and p-values
- Data quality reports

---

### [04 - Lab 3: Light Curve Analysis](./04-lab3-light-curves)
**Time Series Analysis of Astronomical Transients**

This project analyzes light curves (time-series brightness variations) of astronomical objects. It employs rolling median filters, statistical smoothing, and transient detection algorithms to identify and characterize variability in the data.

**Key Topics:**
- Time series data processing
- Rolling window filters and smoothing techniques
- Fourier analysis and periodogram methods
- Transient detection and characterization
- Uncertainty propagation in time-domain data

**Key Outputs:**
- Processed light curves with smoothing
- Power spectral density estimates
- Periodogram analysis for periodic signals
- Transient event detection reports

---

### [05 - Lab 4: Exoplanet Detection via Radial Velocity](./05-lab4-exoplanets)
**Multi-Planet System Characterization Using Spectroscopic Data**

A detailed analysis of exoplanet systems using radial velocity (RV) measurements from high-resolution spectroscopy (HARPS and HIRES instruments). The project fits multiple sinusoidal signals representing gravitational perturbations from planetary companions circling their host stars.

**Key Topics:**
- Radial velocity planet detection methods
- Multi-planet system fitting
- Bayesian parameter space exploration
- Jitter characterization and noise modeling
- Period and semi-amplitude estimation from spectroscopy

**Key Outputs:**
- Fitted orbital parameters (periods, amplitudes, phases)
- Planet mass estimates
- RV residuals and fit quality metrics
- Multi-planet correlation plots (corner plots)

---

## 🛠️ Technical Stack

These projects utilize:

- **Python 3.x** - Primary programming language
- **NumPy** - Numerical computations
- **SciPy** - Advanced statistical functions (optimization, special functions)
- **Matplotlib** - Data visualization and plotting
- **Pandas** - Data manipulation and analysis
- **Corner** - Parameter space visualization (corner plots)
- **Astropy** - Astronomy-specific utilities
- **scikit-learn** - Additional statistical methods
- **TQDM** - Progress monitoring

## 📊 Common Analysis Patterns

All projects share common statistical methodologies:

1. **Data Preparation**
   - Loading and validation of observational data
   - Error/uncertainty quantification
   - Basic statistical summaries

2. **Model Fitting**
   - Least-squares regression methods
   - MCMC parameter exploration
   - Bayesian inference

3. **Visualization**
   - Raw data plots with error bars
   - Model fits overlaid on data
   - Residual analysis plots
   - Corner plots for multi-dimensional parameter spaces
   - Power spectra and periodograms

4. **Validation**
   - Chi-squared tests
   - Residual analysis
   - Model comparison metrics
   - Uncertainty quantification

## 📈 Data Files

Each project directory contains the necessary observational data files:

- **Independent Project**: `m33_data.dat`, `ngc2403_data.dat`, `ngc3198_data.dat`
- **Lab 1**: `data.dat` (SN1a distances and velocities)
- **Lab 2**: Various test datasets and correlation matrices
- **Lab 3**: `data.dat` (time-series photometry)
- **Lab 4**: `HARPS.dat`, `HIRES.dat` (radial velocity measurements)

## 🎓 Educational Value

These projects demonstrate:

- **Practical Implementation** of statistical concepts in astronomy
- **Error Analysis** and propagation of uncertainties
- **Model Building** from physical principles
- **Data Visualization** for scientific communication
- **Bayesian Methods** applied to real observational data
- **Optimization Techniques** for parameter estimation

## 💾 File Organization

```
astrostats-projects/
├── README.md                          (This file)
├── 01-independent-project/
│   ├── README.md                      (Project details)
│   ├── ASTR4303_INDPROJ_Jorge.ipynb   (Main analysis notebook)
│   └── [data files]
├── 02-lab1-hubbles-law/
│   ├── README.md
│   ├── LAB1 - Jorge.ipynb
│   └── [data files]
├── 03-lab2-analysis/
│   ├── README.md
│   ├── ASTR4303_LAB2_Jorge.ipynb
│   └── [data files]
├── 04-lab3-light-curves/
│   ├── README.md
│   ├── ASTR4303_LAB3_Jorge.ipynb
│   └── [data files]
└── 05-lab4-exoplanets/
    ├── README.md
    ├── ASTR4303_LAB4_Jorge.ipynb
    └── [data files]
```

## 🚀 Getting Started

To run these notebooks:

1. **Install Dependencies**
   ```bash
   pip install numpy scipy matplotlib pandas corner astropy scikit-learn tqdm
   ```

2. **Open a Project**
   - Navigate to the project directory
   - Launch Jupyter Notebook: `jupyter notebook`
   - Open the `.ipynb` file

3. **Run Cells**
   - Execute cells in order for proper data flow
   - Some cells may require data files in the directory

## 📝 Notes

- All notebooks include extensive comments explaining the methodology
- Error analysis is performed throughout
- Results are visualized with publication-quality plots
- Projects include both exploratory and confirmatory analyses

## 🔗 References

Each project builds upon published astronomical methods and data:

- **Lab 1**: Classical cosmology (Hubble, 1929)
- **Independent Project**: Disk models (Freeman, 1970) and dark matter halos (Navarro et al., 1996)
- **Lab 4**: Exoplanet methods from radial velocity surveys (Mayor & Queloz, 1995)

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
