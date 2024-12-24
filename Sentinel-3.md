
# Sentinel-3

### Ocean and Land Colour Instrument (OLCI)

As we open an OLCI product in SNAP, below items can be seen in "Product Explorer" window :

![image](https://github.com/user-attachments/assets/1a78d3d8-62bf-44bb-8c2a-3b6b18a9aef4)

Further clicking the Oa*_radiance we have

![image](https://github.com/user-attachments/assets/5359bc64-1b4e-4e1f-99d8-1fd52eca8265)

with each element to represent a particular band. As an example, the first band "Oa01_radiance (400 nm)" contains 
the top of atmosphere (TOA) radiance for OLCI acquisition band Oa01 at 400.0 nm with a wavelength range of +/- 7.5 nm and a pixel resolution of 4865 x 4091. 
Here, pixels are interpreted as the radiance values measured at the top of Earth's atmosphere measured in $(mW.m^{−2}.sr^{−1}.nm^{−1})$, with $mW$, $m$, $sr$, $nm$ 
represent the milliwatts, meter, steradians and nanometer, respectively.
 
## Appendix

#### - Steradian
![image](https://github.com/user-attachments/assets/49b91715-bff6-4bf7-a266-823bc4bc7035)

A cone representing subset of all possible directions from centre of a sphere. The
intercept area among the cone and the unit sphere is defined as the unit solid angle $\hat{κ}$ and
measured in steradian. In case the cone is projected on a sphere with radi $s$, the solid angle $κ$
is computed by dividing the area of the intercept by radi of the sphere.