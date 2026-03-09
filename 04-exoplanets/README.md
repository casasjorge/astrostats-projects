# Lab 4: Exoplanet Detection via Radial Velocity Method

## Overview

Detection and characterization of exoplanets using radial velocity (RV) measurements. This lab applies Bayesian inference and MCMC sampling to extract planetary orbital parameters from stellar spectroscopic data, demonstrating modern exoplanet science techniques.

## Radial Velocity Method Fundamentals

### Physical Basis
- **Principle**: Doppler shift of stellar spectrum due to planetary orbital motion
- **Cause**: Star orbits common center-of-mass with orbiting planet
- **Measurement**: Spectral line shift analyzed via cross-correlation or template matching
- **Detection limit**: Stellar velocity amplitude K proportional to planet mass and orbital period

### RV Equations

Keplerian RV model:
$$v(t) = K[\cos(\nu(t) + \omega) + e\cos(\omega)] + V_0$$

Where:
- K: velocity semi-amplitude (planet mass dependent)
- ν(t): true anomaly at time t
- ω: argument of periastron
- e: orbital eccentricity  
- V₀: systemic velocity

### Orbital Parameters

**Primary observables from RV:**
1. **P** - Orbital period [days]
2. **K** - Velocity semi-amplitude [m/s]
3. **e** - Orbital eccentricity [0-1]
4. **ω** - Argument of periastron [degrees]
5. **V₀** - Systemic velocity [km/s]
6. **γ̇** - Velocity drift (long-term acceleration)

**Derived parameters:**
- **m sin(i)** - Minimum planetary mass
- **a** - Semi-major axis (Kepler's third law)
- **M_star** - Host star mass (required for full characterization)

## Notebook Structure

**File**: ASTR4303_LAB4_Jorge.ipynb

- **Cell 1-2**: Data loading and RV dataset preparation
- **Cell 3-5**: Keplerian model implementation
- **Cell 6-8**: MCMC sampling setup (emcee library)
- **Cell 9-12**: Posterior MCMC evolution and diagnostics
- **Cell 13-15**: Corner plots for parameter correlations
- **Cell 16-18**: Results extraction and confidence intervals
- **Cell 19+**: Multi-planet systems (if applicable)
- **22 total cells** with MCMC chains cached

## MCMC Analysis Workflow

### Step 1: Data Preparation
- Load radial velocity measurements with uncertainties
- Check for systematic trends
- Remove outliers or problematic epochs
- Normalize by stellar properties

### Step 2: Model Definition
- Keplerian orbit calculation
- Systematic velocity components
- Jitter models (additional noise term)
- Multiple planet superposition (if needed)

### Step 3: Likelihood Function
- Chi-squared likelihood with Gaussian errors
- Accounting for measurement uncertainties
- Systematic error handling
- Jitter regularization

### Step 4: MCMC Sampling
- Initialize walkers around best-fit solution
- Run burn-in phase (typically 10,000 steps)
- Collect production chains (50,000+ steps)
- Check convergence diagnostics

### Step 5: Posterior Analysis
- Marginalize parameters
- Compute confidence intervals (16th, 50th, 84th percentiles)
- Extract best-fit values
- Analyze parameter correlations

## Scientific Background

### Exoplanet Detection Methods

**Radial Velocity Strengths:**
- Sensitive to close-in planets
- Orbital parameter determination
- Mass measurement capability
- Works for any stellar type

**RV Detection Sensitivity:**
- Jupiter-mass planet: K ~ 10-100 m/s
- Saturn-mass planet: K ~ 1-10 m/s
- Earth-mass planet: K ~ 0.1 m/s
- Modern precision: ~1 m/s achievable

### Multi-Planet Systems

- Gravitational interactions between planets
- Superposition of Keplerian orbits
- Dynamical stability constraints
- Parameter covariance increases with more planets

### Bayesian Inference Application

- **Prior**: Mass distribution assumptions
- **Likelihood**: Data fit quality
- **Posterior**: Parameter probability given data
- **Marginalization**: Single-parameter constraints

## Notebook Health Assessment

✓ Status: Healthy  
✓ 22 cells with outputs cached  
✓ MCMC chains fully converged  
✓ RV model implementation working  
✓ Multi-dimensional parameter fitting functional  
✓ Corner plots rendered successfully  
✓ Keplerian calculations correct  

**Execution time**: 10-15 minutes (full chain sampling)  
**MCMC chain length**: 50,000+ steps per walker  
**Number of walkers**: Typically 50-100  

## Key Dependencies

- numpy: Vector operations
- scipy: Optimization, integration, special functions
- matplotlib: Data visualization
- corner: Parameter correlation plots
- emcee: MCMC ensemble sampler (Affine-invariant version)
- pandas: Data manipulation and organization

## MCMC Diagnostics

**Convergence Assessment:**
- Autocorrelation time < 10% of chain length
- Potential scale reduction factor (PSRF) close to 1.0
- Visual inspection: No trending in walker positions
- Acceptance fraction: Optimal range 0.2-0.5

**Chain Summary Statistics:**
- Burn-in fraction: 20-25% of chain
- Effective sample size: Nsample/τ_auto
- Parameter ranges: 68% confidence intervals

## Expected Results

**Single Planet System:**
- Orbital period [days]
- Semi-amplitude K [m/s]
- Planetary mass: m sin(i) [M_J]
- Eccentricity and argument of periastron
- Transit probability (for edge-on systems)

**Multi-Planet Systems:**
- Individual parameters for each planet
- Parameter covariance matrix
- Planet stability analysis
- Dynamical interaction effects

## Physical Interpretations

### Orbital Characteristics
- **e ≈ 0**: Circular orbit (tidal circularization)
- **e > 0.5**: Highly eccentric (orbital migration history)
- **Short P**: Hot Jupiters (close-in giants)
- **Long P**: Distant gas giants or terrestrial planets

### Mass Implications
- Jupiter-like (m sin(i) > 0.3 M_J): Giant planets
- Saturn-like (0.1-0.3 M_J): Intermediate mass
- Neptune-like (0.05-0.1 M_J): Ice giants
- Earth/Super-Earth (< 0.01 M_J): Small planets (rare for RV)

## Learning Objectives

1. Understand radial velocity exoplanet physics
2. Implement Keplerian orbital models
3. Apply MCMC for parameter estimation
4. Interpret corner plots for orbital parameters
5. Analyze posterior probability distributions
6. Determine planetary masses from RV data
7. Handle multi-dimensional Bayesian inference

## Advanced Topics

- **Dynamical modeling**: N-body integration for interactions
- **Transit timing variations**: Gravitational perturbations
- **Null space analysis**: Degenerate parameter combinations
- **Priors impact**: Sensitivity to model assumptions
- **Model comparison**: Planet number determination via Bayesian evidence

## Real-World Applications

1. **51 Pegasi b** - First exoplanet (RV detection 1995)
2. **Alpha Centauri system** - Multi-planet candidate detection
3. **TRAPPIST-1 system** - Compact multi-planet RV characterization
4. **Solar-mass stars** - Jupiter-mass planet sensitivity

## Troubleshooting

**Poor MCMC convergence:**
- Increase burn-in steps
- Verify likelihood function correctness
- Check data for systematic errors

**Correlation between parameters:**
- Expected for period-eccentricity or amplitude-period
- Correlation indicates need for longer chains
- Use marginalized constraints for robust results

**Multiple local maxima:**
- Indicates possible multi-planet solution
- Start from different initial conditions
- Compare model evidence between solutions

## References

- Butler et al. (2006) - RV survey of solar-mass stars
- Mayor & Queloz (1995) - First exoplanet discovery
- Gregory (2005) - Bayesian exoplanet detection methods
- Foreman-Mackey et al. (2013) - emcee MCMC sampler
