# Independent Project: Galaxy Rotation Curves

## Overview

This project analyzes the rotation curves of nearby galaxies to constrain dark matter halo models and galaxy structure. By fitting observational kinematics data to theoretical models, we can determine the mass distribution in galaxies and quantify dark matter.

## Scientific Background

### Galaxy Rotation Curves
- Orbital velocity vs. radius in galactic disks
- Inner regions: stellar/gas dominated
- Outer regions: flat curves indicate dark matter
- Keplerian decline vs. observed flat profiles

### Physical Models

#### Freeman (1970) Exponential Disk
- Radial surface density follows exponential profile
- **Rdisk**: Scale length of disk [kpc]
- **Mdisk**: Total disk mass [M☉]

#### Navarro-Frenk-White (NFW) Dark Matter Halo
- Universal dark matter density profile
- **Rhalo**: Characteristic halo radius [kpc]
- **Mhalo**: Total halo mass [M☉]

## Data Files

- **m33_data.dat** - Messier 33 rotation curve
- **ngc2403_data.dat** - NGC 2403 rotation curve  
- **ngc3198_data.dat** - NGC 3198 rotation curve

Each file: radius [kpc], velocity [km/s], uncertainty [km/s]

## Notebook Structure

**File**: ASTR4303_INDPROJ_Jorge.ipynb

- **20 total cells** with comprehensive analysis
- **Cell 1-3**: Imports and data loading
- **Cell 4-6**: Model definitions (disk and halo)
- **Cell 7-10**: MCMC parameter fitting
- **Cell 11+**: Results and corner plot visualization

## Analysis Methods

- Freeman disk model with Bessel functions
- NFW halo model integration
- Keplerian orbit fitting
- Bayesian MCMC sampling
- Parameter correlation analysis

## Expected Outputs

- Rotation curves with best-fit models
- Corner plots showing parameter distributions
- Residual plots for model validation  
- Mass decomposition (disk vs. halo)

## Notebook Health Assessment

✓ Status: Healthy  
✓ Data files available  
✓ 13 cells with cached outputs  
✓ All major computations cached  
✓ MCMC chains fully sampled  

**Note**: Fresh execution requires 10-15 minutes for MCMC sampling

## Dependencies

- numpy: Array operations
- scipy: Special functions (Bessel), optimization
- matplotlib: Visualization
- corner: Parameter space plots
- tqdm: Progress bars

## File Input Requirements

All three data files must be in the project directory for successful execution.
