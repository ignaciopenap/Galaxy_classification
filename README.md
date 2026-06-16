# Photometric and Morphological Analysis of SDSS Galaxies
Developed by Ignacio Peña

This repository contains a data analysis using a dataset of 100,000 galaxies from the Sloan Digital Sky Survey (SDSS). The main goal of this analysis is to evaluate the photometric and structural properties that differentiate two specific galaxy subclasses: STARFORMING and STARBURST.

## Environment and Tools
The data pipeline and visualizations were built using Python 3, relying on pandas and numpy for data filtering, and matplotlib and seaborn for statistical plotting.

## Data Processing and Key Findings

### 1. Stellar Populations via Color-Color Diagram (u-g vs g-r)
After implementing a cleaning step to remove instrumentation noise and extreme outliers, I calculated the standard u-g and g-r color indices. 

By plotting these features, I found that Starburst galaxies significantly concentrate toward lower color index values (the lower-left region of the plot). This reflects the underlying physics of a recent starburst episode, where massive, young O and B-type stars dominate the spectral energy distribution (SED), shifting the light heavily toward ultraviolet and blue wavelengths compared to regular star-forming galaxies.

### 2. Distance Distribution and Redshift Selection Effects
I used a Kernel Density Estimate (KDE) plot to compare how both populations are distributed across cosmic distances. 

While both classes show a local density peak around redshift z ≈ 0.08, the Starburst curve exhibits a much wider tail extending past z > 0.2. This is a clear manifestation of Malmquist bias; because starburst mechanisms make galaxies intrinsically hyper-luminous, they remain detectable at cosmological distances where standard star-forming galaxies fall below the telescope's detection threshold.

### 3. Apparent Morphological Compactness (Petrosian Radius R50)
Using a boxplot layout with outliers suppressed for clarity, I analyzed the distribution of the Petrosian half-light radius in the r-band (petroR50_r).

The results show that Starburst galaxies are noticeably more compact, with a median radius of ~1.5 arcseconds compared to the ~2.5 arcseconds observed in standard star-forming galaxies. This structural difference aligns with the current understanding that violent starburst phenomena are usually triggered in high-density environments or during galactic interactions that rapidly funnel gas into tight nuclear regions.

---

## Local Replication

To run the pipeline and replicate the plots locally, clone this repository and execute the Jupyter Notebook:

```bash
git clone [https://github.com/ignaciopenap/Galaxy_classification.git](https://github.com/ignaciopenap/Galaxy_classification.git)
cd Galaxy_classification
code .