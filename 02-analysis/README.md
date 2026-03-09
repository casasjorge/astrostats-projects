# Lab 2: Statistical Methods in Astronomy

## Overview

Advanced statistical analysis techniques applied to astronomical data. This lab demonstrates corner plots for parameter space visualization, hypothesis testing, and multi-dimensional probability distributions using real observational datasets.

## Statistical Concepts

### Multi-Dimensional Distributions
- Posterior probability distributions in parameter space
- Covariance structure between fitted parameters
- Confidence interval determination across multiple dimensions
- Marginalization techniques

### Corner Plots (Triangle Plots)
- **Purpose**: Visualize high-dimensional parameter correlations
- **Diagonal**: 1D marginalized posteriors
- **Off-diagonal**: 2D joint distributions
- **Standard tool**: corner.py package

### Hypothesis Testing

1. **Goodness-of-fit**: χ² and K-S tests
2. **Parameter significance**: Normal approximation tests
3. **Model comparison**: Likelihood ratio tests
4. **Bayesian inference**: Prior vs. posterior comparison

## Data Analysis Workflow

**Step 1: Data Quality Assessment**
- Check for outliers and data anomalies
- Examine distribution shapes
- Validate error estimates

**Step 2: Model Fitting**
- Define likelihood functions
- Initialize parameter guesses
- Perform optimization/sampling

**Step 3: Uncertainty Characterization**
- Bootstrap resampling
- Covariance matrix analysis
- Confidence region calculation

**Step 4: Visualization**
- Corner plots for parameter space
- Residual diagnostics
- Data-model comparison plots

## Notebook Structure

**File**: ASTR4303_LAB2_Jorge.ipynb

- **Cell 1-3**: Data loading and preprocessing
- **Cell 4-6**: Exploratory statistics analysis
- **Cell 7-10**: Parameter fitting procedures
- **Cell 11-14**: Corner plot generation (multi-panel visualization)
- **Cell 15+**: Hypothesis testing and validation
- **18 total cells** with comprehensive outputs

## Corner Plot Interpretation

- **Diagonal panels**: Marginalized posterior for each parameter
  - 1-sigma confidence intervals marked
  - Distribution shape (Gaussian vs. non-Gaussian)
  
- **Off-diagonal panels**: Joint 2D distributions
  - Parameter correlations visible
  - Covariance structure revealed
  - Ellipse orientation shows correlation strength

## Notebook Health Assessment

✓ Status: Healthy  
✓ 18 cells with outputs cached  
✓ Corner plots fully rendered  
✓ Statistical tests completed  
✓ Multi-dimensional analysis functional  
✓ Visualization library (corner) working  

**Execution time**: 2-3 minutes  
**Memory usage**: Moderate (< 500MB)  

## Dependencies

- numpy: Array operations and linear algebra
- scipy: Statistical functions, optimization
- matplotlib: Basic plotting
- corner: Advanced corner plot generation
- pandas: Data frames and statistics

## Key Analyses Performed

1. Distribution analysis of multiple astronomical parameters
2. Parameter correlation determination
3. Significance testing for fitted values
4. Confidence contour identification
5. Model selection via Bayesian comparison

## Statistical Tests Included

- Kolmogorov-Smirnov goodness-of-fit
- Chi-squared parameter significance
- Likelihood ratio model comparison
- Bootstrap confidence intervals
- Covariance-based uncertainty estimation

## Expected Outputs

- Multi-parameter corner plots with 18-36 panels
- Statistical summary tables
- 1D and 2D confidence intervals
- Hypothesis test p-values
- Model comparison statistics

## Learning Objectives

1. Create and interpret corner plots
2. Understand parameter correlations
3. Perform hypothesis testing
4. Extract confidence intervals from samples
5. Compare competing statistical models
6. Visualize high-dimensional probability distributions

## Advanced Features

- Contour level configuration (1, 2, 3-sigma)
- Custom axis labeling
- Correlation coefficient display
- Quantile calculation and display
- Truths/known values overlay

## Troubleshooting

**Corner plot not displaying**: Ensure corner package installed
**Statistical test failures**: Check data for NaN/Inf values
**Memory issues**: Reduce sample size for visualization
