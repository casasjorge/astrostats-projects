# Lab 1: Hubble's Law and the Expansion of the Universe

## Overview

This fundamental observational astronomy lab determines the Hubble constant (H₀) by measuring distances and recession velocities of nearby galaxies. Linear regression analysis yields the expansion rate of the universe.

## Scientific Concepts

### Hubble's Law
- **Observation**: $v = H_0 \times d$
- **Interpretation**: Universe expanding uniformly
- **Hubble Constant**: $H_0 \approx 70$ km/s/Mpc (modern value)
- **Expansion Age**: $\tau_0 = 1/H_0 \approx 14$ billion years

### Distance Measurement Techniques

1. **Parallax measurements** - geometric distance from base angle
2. **Cepheid distance ladders** - variable star period-luminosity relation
3. **Spectral redshift** - recession velocity from Doppler shift

### Cosmological Implications

- Hubble expansion discovered by Edwin Hubble (1929)
- Observational foundation of Big Bang cosmology
- Directly constrains universe age and expansion history

## Data Content

Galaxy data includes:
- **NAME**: Galaxy identifier
- **DISTANCE**: Distance in Megaparsecs [Mpc]
- **RECESSION_VELOCITY**: Redshift velocity [km/s]
- **UNCERTAINTY**: Measurement uncertainty bands

## Notebook Structure

**File**: LAB1 - Jorge.ipynb

- **Cell 1**: Data import and preprocessing
- **Cell 2**: Exploratory data visualization
- **Cell 3**: Linear regression analysis
- **Cell 4**: Residual diagnostics
- **Cell 5**: Parameter extraction and H₀ calculation
- **Cell 6**: Error propagation analysis
- **12 cells** with all outputs cached

## Analysis Workflow

1. Load galaxy distance and velocity datasets
2. Create scatter plot with error bars
3. Perform least-squares linear regression
4. Extract slope (H₀) and uncertainty
5. Compare to current accepted value
6. Analyze residual distributions

## Expected Results

- **Hubble Constant**: $H_0 \approx 60-80$ km/s/Mpc range
- **R² value**: Typically > 0.85 for modern data
- **Age estimate**: ~14-18 billion years

## Notebook Health

✓ Status: Healthy  
✓ Linear regression working  
✓ 12 cells with outputs  
✓ All visualizations present  
✓ Ready for quick review  

**Execution time**: < 1 minute

## Key References

- Hubble, E. P. (1929) - Original distance-velocity relation
- Friedmann-Robertson-Walker model - Expansion equations
- Cosmic distance ladder - Multiple measurement techniques

## Technical Stack

- numpy: Linear algebra
- scipy.stats: Regression and statistics  
- matplotlib: Publication-quality plots
- pandas: Data manipulation

## Learning Objectives

1. Understand observational data analysis workflow
2. Apply linear regression to cosmological data
3. Extract physical parameters from astronomical measurements
4. Interpret confidence intervals and uncertainty

## Troubleshooting

If galaxy data fails to load:
- Check CSV formatting (comma-separated values)
- Verify column names match expected headers
- Ensure decimal notation (periods, not commas)
