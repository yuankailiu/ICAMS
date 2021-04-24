[![Language](https://img.shields.io/badge/python-3.5%2B-blue.svg)](https://www.python.org/)
[![Citation](https://img.shields.io/badge/doi-10.1016%2Fj.jgr.solidearth.2020JB020952-blue)](https://doi.org/10.1029/2020JB020952)


# ICAMS

An open source module in python for InSAR troposphere Correction using global Atmospheric Models that considers the spatial Stochastic properties of the troposphere (ICAMS). We model (funcitonal model + stochatic model) the tropospheric parameters (P,T, and e) layer by layer along the altitude levels, and we calculate the InSAR delays along the LOS direction. ICAMS can be applied with all of the weather models (global or local). Currently, our code support to download and process [ERA5 reanalysis data](https://retostauffer.org/code/Download-ERA5/) from ECMWF, and ICAMS can be used with [MintPy](https://github.com/insarlab/MintPy) hdf5 outputs directly.

This is research code provided to you "as is" with NO WARRANTIES OF CORRECTNESS. Use at your own risk.

The key steps of ICAMS can be summarized as follow: <br> 

step 1: Download weather model data [Make sure you have updated the user.cfg file].\
Step 2: Pre-processing of GAM outputs (P-layers to H-layers)\
Step 3: Estimating LOS locations at different altitude layers [You need to input slc.par file to provide orbit data] \
Step 4: Predicting trop-parameters at LOS locations (SKlm) [Make sure you have [PyKrige](https://pypi.org/project/PyKrige/) module available] \
Step 5: Calculating LOS delays \
Step 6: Interpolating LOS delays (SKlm) layer by layer \
Step 7: Interpolating SAR/InSAR tropospheric delays [Make sure you have [elevation](https://pypi.org/project/elevation/) available and download the global geoid data] 



Citation: [Cao, Y.M., Jónsson, S., Li, Z.W., 2021, Advanced InSAR Tropospheric Corrections from Global Atmospheric Models that Incorporate Spatial Stochastic Properties of the Troposphere, Journal of geophysical research: solid earth, doi: 10.1029/2020JB020952](https://agupubs.onlinelibrary.wiley.com/doi/10.1029/2020JB020952)

******* ICAMS is still under development, and we will keep going to make it user friendly ******
