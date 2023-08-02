# Equivalent water thickness/canopy water content from hyperspectral data

This tutorial shows how to calculate equivalent water thickness or canopy water content (CWC) from [AVIRIS-NG](https://daac.ornl.gov/cgi-bin/dataset_lister.pl?p=47) data. Variation in CWC can indicate drought stress and wildfire risk.

We will apply a simple fitting of spectral absorption features of liquid water and use scripts available from [ISOFIT package](https://github.com/isofit/isofit/tree/main).

## Canopy Water Content (CWC)
First, surface reflectance was derived using the Optimal Estimation-based simultaneous modeling of surface and atmosphere through the ISOFIT codebase. Derived surface reflectance spectra were particularly smooth in water absorption bands and include estimates of per-band posterior uncertainties (Thompson et al. 2018).

The CWS was then derived from surface reflectance by applying a well-validated algorithm based on a physical model (Beer-Lambert model) (Green et al. 2006; Bohn et al. 2020). Of note, this model does not account for multiple scattering effects within the canopy and may result in overestimation of retrieved CWC (Bohn et al. 2020).


## References

- Bohn, N., L. Guanter, T. Kuester, R. Preusker, and K. Segl. 2020. Coupled retrieval of the three phases of water from spaceborne imaging spectroscopy measurements. Remote Sensing of Environment 242:111708. https://doi.org/10.1016/j.rse.2020.111708
- Green, R.O., T.H. Painter, D.A. Roberts, and J. Dozier. 2006. Measuring the expressed abundance of the three phases of water with an imaging spectrometer over melting snow. Water Resources Research 42:W10402. https://doi.org/10.1029/2005WR004509
- Thompson, D.R., V. Natraj, R.O. Green, M.C. Helmlinger, B.-C. Gao, and M.L. Eastwood. 2018. Optimal estimation for imaging spectrometer atmospheric correction. Remote Sensing of Environment 216:355–373. https://doi.org/10.1016/j.rse.2018.07.003

## Datasets
- Brodrick, P.G., R. Pavlick, K.D. Chadwick, and Jet Propulsion Laboratory. 2023. SHIFT: AVIRIS-NG L1A Unrectified Radiance. ORNL DAAC, Oak Ridge, Tennessee, USA. https://doi.org/10.3334/ORNLDAAC/2184
- Brodrick, P., R. Pavlick, K.D. Chadwick, and Jet Propulsion Laboratory. 2023. SHIFT: AVIRIS-NG L2A Unrectified Reflectance. ORNL DAAC, Oak Ridge, Tennessee, USA. https://doi.org/10.3334/ORNLDAAC/2183
-  Bohn, N., P.G. Brodrick, and K.D. Chadwick. 2023. SHIFT: AVIRIS-NG Derived Gridded Mosaicked Canopy Water Content, California, 2022. ORNL DAAC, Oak Ridge, Tennessee, USA. https://doi.org/10.3334/ORNLDAAC/2242
