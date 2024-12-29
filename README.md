# Obtained products from Sentinel-3
### Ocean and Land Colour Instrument (OLCI) 
( i ) Land surface reflectance full/reduced resolution (LFR/LRR)

( ii ) Water surface reflectance full/reduced resolution (WFR/WRR)
  
### Land Surface Temperature Radiometer (SLSTR)

( iii ) Land surface temprature (LST)

( iv ) Sea surface temperature products (WST)

# --------------------------------------------------------------------
## ( i ) Land surface reflectance, full resolution (LFR)
# --------------------------------------------------------------------

As we open the product in SNAP we obtain below structure

<p align="left">
  <img src="https://github.com/user-attachments/assets/f92e4a62-37e5-4c1d-86b5-78a73ef03813" width="150" height="350">
</p>

Under the "Band", we obtain five main categories "IWV", "OGVI", "OTCI", "RC681" and "RC865". They represent 

+ Integrated Water Vapor (IWV) : the total water vapor content in a vertical column of the atmosphere measured in (mm).
+ Global Vegetation Index (OGVI) : provides information about the density and vigor of green vegetation and has no unit measure.
+ Terrestrial Chlorophyll Index (OTCI) : can be used to assess chlorophyll content over land to explore vegetation health.
+ RC681 and RC865 : Both are rectified reflectances for bands O10 and O17, respectively measured in $(mW.m^{−2}.sr^{−1}.nm^{−1})$, with $mW$, $m$, $sr$, $nm$ 
represent the milliwatts, meter, steradians and nanometer, respectively.

In addition, there are three more categories, namely $\lambda_0$, FWHM, and solar_flux that we explain them later on. 

Also, under the "Masks" we get a set of flag-elements that provide more informations on the classified type of scene in pixel level, namely land, water etc.

## Area of study

Our area of interest is the Kakadu National Park [1], located on north side of Australia. We proceed to visualize few indices from OLCI

### Visualisation of OTCI index

The OTCI index measures the photosynthetic activity of plants and is sensitive to vegetation health, and growth stages.
<p align="center">
  <img src="https://github.com/user-attachments/assets/f30d081d-2d3f-457e-b587-9c44841a7be2" width="350" height="350">
  <img src="https://github.com/user-attachments/assets/fdfe91f8-a5c3-45cd-939a-e82d61fe7d4f" width="350" height="350">
</p>

(Left) The OTCI band shown with no colormap used. The red, light blue and dark blue color coded areas to represent the failed to measured areas, the 
clouds and the ocean. (Right) The OTCI band color coded with darker green values represent areas with more photosynthetic activities where as light 
green areas show less active area concerning such activities.

## Visualisation of WVI index

The Water Vapour Index (WVI) used in assessing moisture content in vegetation environment. 
<p align="center">
  <img src="https://github.com/user-attachments/assets/10f8889b-680f-4a75-8a3c-07bd7045a88a" width="320" height="320">
  <img src="https://github.com/user-attachments/assets/56b9332b-4947-49ab-b972-a66c3d9765d0" width="320" height="320">
  <img src="https://github.com/user-attachments/assets/3d35ce2d-fbe7-41aa-9a82-50bcc7622fc2" width="175" height="135">
</p>
(Left) The WVI band color coded in Jet. (Right) The same band after performing histogram equalization. The more blue, 
the higher is the content of water vapor. 

## Visualisation of OGVI index
The OGVI index assess vegetation health and density based on the amount of green vegetation in area.
<p align="center">
  <img src="https://github.com/user-attachments/assets/81fbb9ae-3b18-47d8-b19c-b847f4ae4edf" width="320" height="320">
  <img src="https://github.com/user-attachments/assets/1b2fc62a-27b7-49f5-b42d-ec7f1737588b" width="320" height="320">
  <img src="https://github.com/user-attachments/assets/d5a92987-66b1-4882-9b32-3ec403695092" width="175" height="135">
</p>
(Left) The OGVI band color coded. (Right) The same band after performing histogram equalization. The image is sensed around 
May 2016 at the time when the reasning season just ended. This means, the area is being most probably observed raining during 
past raining season November to April 2016. The more blue, means the more vegetation texture is observed.

## RC681 / RC865 bands

<p align="center">
  <img src="https://github.com/user-attachments/assets/b610ed22-d3ab-499a-bd3f-a55d2e56f7de" width="350" height="350">
  <img src="https://github.com/user-attachments/assets/2d5f8a61-2f41-49f2-b0da-36ea0b83c586" width="350" height="350">
</p>
Rectified reflectance values for the bands (Left) O10 and (Right) O17. Note, the light and the dark blue represent the cloud and the water areas.

# --------------------------------------------------------------------
## ( ii ) Water surface reflectance, full resolution (WFR)
# --------------------------------------------------------------------

## A865 band

<p align="center">
  <img src="https://github.com/user-attachments/assets/92bf5e0a-998d-4abf-8c58-ec743829aea3" width="350" height="350">
  <img src="https://github.com/user-attachments/assets/e74a9855-222d-4ffe-8fbf-27cb94b5b327" width="350" height="350">
  <img src="https://github.com/user-attachments/assets/1ddad9d6-caa2-4174-ba9c-7bc2386baade" width="150" height="350">
</p>
(Left) The RGB image comprosed of bands O8, O6 and O4 as red, green and blue respectively. (Middle) The A865 band color coded with 
"Aerosol optical thickness" scheme. The vast green area represents the land and the brown strip is the clouded costal area. The values 
corresponding to the shown middle image are presented in (Right).

# --------------------------------------------------------------------
## Level 1 product
# --------------------------------------------------------------------

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

# References 
[1] https://en.wikipedia.org/wiki/Kakadu_National_Park

# Appendix

#### - Steradian
<p align="center">
  <img src="https://github.com/user-attachments/assets/49b91715-bff6-4bf7-a266-823bc4bc7035" width="250" height="250">
</p>

A cone representing subset of all possible directions from centre of a sphere. The
intercept area among the cone and the unit sphere is defined as the unit solid angle $\hat{κ}$ and
measured in steradian. In case the cone is projected on a sphere with radi $s$, the solid angle $κ$
is computed by dividing the area of the intercept by radi of the sphere.

