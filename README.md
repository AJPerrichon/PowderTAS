# PowderTAS
![alt text](https://zenodo.org/badge/DOI/10.5281/zenodo.3371370.svg)

The "powderTAS" Matlab code calculates neutron scattering cross-sections of powder samples, represented as Q-E scattering maps, using "single-crystal" phonon calculation eigenvectors as input. The name comes from the original not-to-be-repeated neutron experiment where we put a powder sample on a three-axis spectrometer (TAS). The whole concept of this code is to do a powder average over a high-number of Q-points, randomly generated at a distance |Q| from the origin, forming a sphere (the positive quadrant of it). At each point on this sphere, the eigenvectors are obtained by trilinear interpolation, and using them, the scattering cross-sections (elastic and inelatic, coherent and incoherent) are calculated. These cross-sections are then used to make an histrogram-spectra, which can be seen as a line in a frequency/momentum map. This process is repeated for a serie of Q-values, hence forming the complete scattering map of a powder sample.
The PowderTAS script and its functions are in the Matlab live script format, and commented therein.

**2019-08-22.**
The "powdertas_interpolate_eigenvectors" has been updated. The qmesh is now shrinked to the positive quadrant before the interpolation, which massively speeds up this step, from 140 to 55 seconds for Nvec=1e5. The header of the main file has been updated accordingly.

*Example: The neutron-weighted scattering map of a powder sample of BaZrO3.*
![alt text](https://imgshare.io/images/2019/08/22/logo.png)
