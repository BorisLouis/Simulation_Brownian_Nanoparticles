Simulates fluorescent particles undergoing Brownian motion and generates synthetic microscopy images according to user input.

*Pipeline*
1) Simulate 3D Brownian motion (x, y, z, t) from physical parameters (D, viscosity, temperature)
2) Render each frame: each particles is a 3d dirac function with given intensity to which a 3D Airy-disk PSF (defocus-aware) is convolved.
3) Add Poisson shot noise + Gaussian read-out noise
4) Save as 16-bit grayscale TIFF (ImageJ-compatible)

*How to use*

1)Connect to GPU runtime in google colab

2)Change REPO_DIR to desired path in your google drive

3)Change parameters in section 2 according to desired simulation

4)Press run all

5)Allow access to google drive

6)Results (Simulated Movie + simulated particles traces) will be stored at REPO_DIR/Results



Remark: The objects are simulated as dimensionless (1 single bright pixel to which a PSF is convolved), hence if the dimensions chosen of the object are not realistic (e.g. 1um particles), the diffusion dynamic will be properly simulated but the images would look like a diffraction limited object movie slow.
