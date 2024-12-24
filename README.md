
# Sentinel-3

### Ocean and Land Colour Instrument (OLCI)

As we open an OLCI product in SNAP, below items can be seen in "Product Explorer" window :

![image](https://github.com/user-attachments/assets/1a78d3d8-62bf-44bb-8c2a-3b6b18a9aef4)

### Radiance
Further clicking the Oa*_radiance we have

![image](https://github.com/user-attachments/assets/5359bc64-1b4e-4e1f-99d8-1fd52eca8265)

with each element to represent a particular band. As an example, the first band "Oa01_radiance (400 nm)" contains 
the top of atmosphere (TOA) radiance for OLCI acquisition band Oa01 with central wavelength of 400.0 (nm) with a wavelength range of +/- 7.5 (nm) and a pixel resolution of $4865\times 4091$. 
Here, pixels are interpreted as the radiance values measured at the top of Earth's atmosphere measured in $(mW.m^{−2}.sr^{−1}.nm^{−1})$, with $mW$, $m$, $sr$, $nm$ 
represent the milliwatts, meter, steradians and nanometer, respectively.

### Central wavelength of each band $\left(\lambda_0\right)$
Under the Band, clicking "lambda0", we obtain again $21$ number of elements, each of size $4865\times 4091$ pixels, called "lambda0_band_1" till "lambda0_band_21". 

![image](https://github.com/user-attachments/assets/9622169f-8a36-4f92-8ba3-017317f86d61)

The first band contains the central wavelength of 400.0 (nm) with a wavelength range of +/- 7.5 (nm), more precisely the values in range of 392.5 to 407.5 (nm).

### Full Width at Half Maximum (FWHM) 

## Appendix

#### - Steradian
![image](https://github.com/user-attachments/assets/49b91715-bff6-4bf7-a266-823bc4bc7035)

A cone representing subset of all possible directions from centre of a sphere. The
intercept area among the cone and the unit sphere is defined as the unit solid angle $\hat{κ}$ and
measured in steradian. In case the cone is projected on a sphere with radi $s$, the solid angle $κ$
is computed by dividing the area of the intercept by radi of the sphere.
