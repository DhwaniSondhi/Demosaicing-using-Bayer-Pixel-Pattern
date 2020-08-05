## Demosaicing-using-Bayer-Pixel-Pattern
This is the assignment of COMP6341 COMPUTER VISION. The aim of this assignment is to convert the Bayer pixel pattern into a RGB representation where each pixel has red, green and blue color channels. 

### Basics
This algorithm is the first step of the imaging pipeline that reconstructs a full-colored image from the raw output of the digital camera’s sensor. The assignment was divided into two parts.

### Part A:
- Implemented a Simple linear Interpolation by averaging four or two nearest neighbours. 
- Built a kernel for each channel in following way.
<img src="https://github.com/DhwaniSondhi/Demosaicing-using-Bayer-Pixel-Pattern/blob/master/images/1.PNG" alt="alt" width="800" height="300"/><br/>
- Found root squared difference between original and reconstructed images.

### Part B:
- Implemented an improved approach: Simple Bilinear Interpolation.
- This interpolation works for better for R values as R channel is sampled at a higher rate than the G and B channels.
- Computed difference images G-R and B-R between the respective interpolated channels.
- Used median filtering to eliminate splotches.
- Created modified G and B channels by adding the R channel to the difference images.
- Output created is better than Part A.

### How to run?
- Set up an environment and install for **python file (code.py)**: OpenCV & numpy and for **Jupyter Notebook**: OpenCV, MatplotLib & numpy.
- Please keep the required images in the same folder as the code.
- Please mention the input and output file name with extensions.
- In both cases, 2 images are generated.
- The first image for each Part contains the actual, output and 3-channel noise image(noise divided in 3 channels).
- The second image for each Part is the 1-channel noise image(Grey scale-noise accumulated in 1 channel).
- Both images are described as Part A or B.
- The images can be closed by pressing any keyboard key and will be saved in the same folder for reviewal.

### Output
| Input  | Output |
| ------------- | ------------- |
| <img src="https://github.com/DhwaniSondhi/Demosaicing-using-Bayer-Pixel-Pattern/blob/master/images/crayons_mosaic.bmp" alt="alt" width="300" height="300"/> | <img src="https://github.com/DhwaniSondhi/Demosaicing-using-Bayer-Pixel-Pattern/blob/master/images/crayons.jpg" alt="alt" width="300" height="300"/> |
| <img src="https://github.com/DhwaniSondhi/Demosaicing-using-Bayer-Pixel-Pattern/blob/master/images/oldwell_mosaic.bmp" alt="alt" width="300" height="300"/> | <img src="https://github.com/DhwaniSondhi/Demosaicing-using-Bayer-Pixel-Pattern/blob/master/images/oldwell.jpg" alt="alt" width="300" height="300"/> |
| <img src="https://github.com/DhwaniSondhi/Demosaicing-using-Bayer-Pixel-Pattern/blob/master/images/pencils_mosaic.bmp" alt="alt" width="300" height="300"/> | <img src="https://github.com/DhwaniSondhi/Demosaicing-using-Bayer-Pixel-Pattern/blob/master/images/pencils.jpg" alt="alt" width="300" height="300"/> |

[Please click here for more assignment description.](https://github.com/DhwaniSondhi/Demosaicing-using-Bayer-Pixel-Pattern/blob/master/Assignment.pdf)
