# Lab 3: Time-Series Analysis and Light Curve Photometry

## Overview

Analysis of time-domain astronomical observations through light curve study. This lab focuses on detecting periodic behavior, filtering noise, and characterizing variable stars using Fourier methods and light curve decomposition techniques.

## Time-Domain Astronomy Concepts

### Light Curves
- **Definition**: Flux vs. time for astronomical objects
- **Applications**: Variable star classification, exoplanet transit detection, transient events
- **Data**: Magnitude, flux density, or intensity over observation period

### Periodicities

1. **Intrinsic Variables**
   - Pulsating stars (δ Scuti, RR Lyrae)
   - Rotation modulation
   - Orbital motion (eclipsing binaries)

2. **Extrinsic Variables**
   - Transits (planetary or stellar)
   - Eclipses (binary systems)
   - Microlensing events

### Analysis Methods

**Fourier Analysis**
- Power spectral density computation
- Frequency domain identification of periodicities
- Detection of harmonic structure

**Filtering Techniques**
- High-pass filtering: Remove long-term trends
- Low-pass filtering: Reduce noise
- Band-pass filtering: Isolate specific frequencies
- Moving average smoothing

**Statistical Characteristics**
- Periodogram analysis
- Lomb-Scargle periodogram (unevenly sampled data)
- Autocorrelation functions
- Variance decomposition

## Notebook Structure

**File**: ASTR4303_LAB3_Jorge.ipynb

- **Cell 1**: Data loading and time-series preparation
- **Cell 2-3**: Exploratory visualization
- **Cell 4-6**: Fourier analysis and periodogram
- **Cell 7-9**: Filtering operations (high/low-pass)
- **Cell 10-12**: Period detection and significance testing
- **Cell 13-15**: Transient/event identification
- **Cell 16+**: Summary statistics and interpretation
- **19 total cells** with cached computation results

## Data Content

Typical light curve data includes:
- **TIME**: Julian Date or phases [days, hours]
- **FLUX/MAGNITUDE**: Brightness measurement
- **ERROR**: Photometric uncertainty
- **FLAGS**: Data quality indicators

## Analysis Workflow

### Step 1: Time-Series Preparation
- Check for temporal gaps
- Handle missing observations
- Convert between magnitude/flux scales
- Normalize and detrend

### Step 2: Fourier Analysis
- Compute power spectrum
- Identify dominant frequencies
- Assess statistical significance
- Detect harmonic content

### Step 3: Filtering & Smoothing
- Remove high-frequency noise
- Extract long-term trends
- Identify outliers/transients
- Characterize noise properties

### Step 4: Periodicity Detection
- Lomb-Scargle periodogram for unevenly sampled data
- Peak significance assessment
- Period fold and phase analysis
- Harmonic series identification

### Step 5: Interpretation
- Classification by variability type
- Parameter extraction (period, amplitude)
- Event timing determination
- Comparison to templates

## Notebook Health Assessment

✓ Status: Healthy  
✓ 19 cells with outputs cached  
✓ Time-series data loading functional  
✓ Fourier analysis complete  
✓ Filtering methods implemented  
✓ Periodogram generation working  
✓ Transient detection functional  

**Execution time**: 3-5 minutes  
**Data requirements**: Light curve file(s) in time-flux format  

## Key Dependencies

- numpy: Array operations and mathematical functions
- scipy.signal: FFT, filtering, Lomb-Scargle periodogram
- scipy: Special functions, optimization
- matplotlib: Time-series and spectral visualizations
- pandas: Data organization

## Spectral Analysis Techniques

1. **Discrete Fourier Transform (DFT)**
   - Even sampling required
   - Computational efficiency: O(N log N)
   - Power spectrum visualization

2. **Lomb-Scargle Periodogram**
   - Handles irregular time sampling
   - No window function artifacts
   - Statistical significance testing

3. **Autocorrelation Analysis**
   - Pattern repetition detection
   - Lag structure identification
   - Trend vs. cyclical decomposition

## Visualization Outputs

- Time-series plot with error bands
- Power spectrum with significance levels
- Periodogram with peak identification
- Phase-folded light curves
- Filtered time-series comparison
- Autocorrelation function plots

## Scientific Applications

1. **Variable Star Classification**
   - Period determines star type (Cepheidδ, RR Lyrae, etc.)
   - Amplitude indicates physical properties
   - Fourier modes reveal internal structure

2. **Exoplanet Transits**
   - Periodic flux dips from planetary occultation
   - Transit timing variations (TTV)
   - Atmosphere characterization

3. **Binary Star Evolution**
   - Eclipse timing precision
   - Orbital period measurement
   - Mass function determination

## Expected Results

- Detected period(s) in observed light curve
- Significance measurements (S/N ratio, p-values)
- Filtered time series with reduced noise
- Phase-folded periodic signal
- Frequency spectrum with harmonic identification

## Learning Objectives

1. Analyze time-domain astronomical data
2. Apply Fourier analysis to detect periodicities
3. Implement digital filtering techniques
4. Significance test for detected periods
5. Classify variable phenomena
6. Extract physical parameters from timing

## Troubleshooting

- **Poor frequency resolution**: Too short observation span
- **Aliasing artifacts**: Sampling faster than Nyquist rate
- **Missing peaks**: Try Lomb-Scargle for irregular data
- **High noise floor**: Apply appropriate filtering before analysis

## References

- Press et al. "Numerical Recipes" - Signal processing methods
- Press & Rybicki (1989) - Lomb-Scargle periodogram
- Scargle (1982) - Period analysis of unevenly spaced observations
