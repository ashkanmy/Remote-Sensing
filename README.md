# Ocean and Land Colour Instrument (OLCI) obtained from Sentinel-3

## Level-2 product

As we open an OLCI Level-2 product in SNAP we obtain below structure

<p align="left">
  <img src="https://github.com/user-attachments/assets/f92e4a62-37e5-4c1d-86b5-78a73ef03813" width="150" height="350">
</p>

Under the "Band", we obtain four main categories "IWV", "OGVI", "OTCI", "RC681" and "RC865". They represent 

+ Integrated Water Vapor (IWV) : the total water vapor content in a vertical column of the atmosphere measured in (mm).
+ Optical Green Vegetation Index (OGVI) : provides information about the density and vigor of green vegetation and has no unit measure.
+ Ozone Total Column Index (OTCI) : Measures the total ozone content in the atmospheric column with a measure of Dobson Units (DU), where
  1 DU = 0.01 (mm) of ozone at standard temperature and pressure.
+ RC681 and RC865 : Both are Rayleigh-corrected reflectance values, but they correspond to different wavelengths and serve different purposes based on
  their spectral characteristics. Their measure unit is $(mW.m^{−2}.sr^{−1}.nm^{−1})$, with $mW$, $m$, $sr$, $nm$ 
represent the milliwatts, meter, steradians and nanometer, respectively.

In addition, there are three more categories, namely $\lambda_0$, FWHM, and solar_flux that we explain them later on. 

Also, under the "Masks" we get a set of flag-elements that provide more informations on the classified type of scene in pixel level, namely land, water etc.

## Level-1 product

As we open an OLCI product in SNAP, below items can be seen in "Product Explorer" window :

<p align="left">
  <img src="https://github.com/user-attachments/assets/1a78d3d8-62bf-44bb-8c2a-3b6b18a9aef4" width="150" height="350">
</p>

### Radiance
Further clicking the Oa*_radiance we have

<p align="left">
  <img src="https://github.com/user-attachments/assets/5359bc64-1b4e-4e1f-99d8-1fd52eca8265" width="150" height="350">
</p>

with each element to represent a particular band. As an example, the first band "Oa01_radiance (400 nm)" contains 
the top of atmosphere (TOA) radiance for OLCI acquisition band Oa01 with central wavelength of 400.0 (nm) with a wavelength range of $\pm 7.5$ (nm) and a pixel resolution of $4865\times 4091$. 
Here, pixels are interpreted as the radiance values measured at the top of Earth's atmosphere measured in $(mW.m^{−2}.sr^{−1}.nm^{−1})$.

### Central wavelength of each band $\left(\lambda_0\right)$
Under the Band, clicking "lambda0", we obtain again $21$ number of elements, each of size $4865\times 4091$ pixels, called "lambda0_band_1" till "lambda0_band_21". 

<p align="left">
  <img src="https://github.com/user-attachments/assets/9622169f-8a36-4f92-8ba3-017317f86d61" width="150" height="350">
</p>

As an example, the first band contains the central wavelength of 400.0 (nm) with a wavelength range of $\pm 7.5$ (nm), more precisely the values in range of 392.5 to 407.5 (nm).

### Full Width at Half Maximum (FWHM) 

Taking the maximum value of all the wavelengths corresponding to a band establshing a statistical distribution and divide it by half, two “half maximum value” points 
are obtained. The width between these two points on the distribution curve represents the FWHM measurement. Each of $21$ bands has a corresponding matrix of size 
$4865\times 4091$ containing the pixel-deüendent FWHM values.

<p align="left">
  <img src="https://github.com/user-attachments/assets/aa75c842-b4c1-4709-b79f-2f25f4a76e13" width="150" height="350">
</p>

# Level-2 Processing

## Area of study

Our area of interest is the Kakadu National Park [1], located on north side of Australia. We proceed to visualize few elements from OLCI at level-2.

### Visualisation of OTCI index
<p align="center">
  <img src="https://github.com/user-attachments/assets/19730bf9-86d7-4901-ad05-2582886ca06f" width="350" height="350">
  <img src="https://github.com/user-attachments/assets/f30d081d-2d3f-457e-b587-9c44841a7be2" width="350" height="350">
</p>
(Left) The OTCI band. (Right) The labeled OTCI band with red, light blue and dark blue color coded areas to represent the failed to measured 
ozone areas, the clouds and the ocean.

# References 
[1] https://en.wikipedia.org/wiki/Kakadu_National_Park

# Appendix

#### - Steradian
<p align="center">
  <img src="https://github.com/user-attachments/assets/49b91715-bff6-4bf7-a266-823bc4bc7035" width="350" height="350">
</p>

A cone representing subset of all possible directions from centre of a sphere. The
intercept area among the cone and the unit sphere is defined as the unit solid angle $\hat{κ}$ and
measured in steradian. In case the cone is projected on a sphere with radi $s$, the solid angle $κ$
is computed by dividing the area of the intercept by radi of the sphere.

