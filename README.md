# Digitizing Old Physical Photographs
This project focuses on developing a solution for digitizing and restoring old physical photographs using a combination of traditional computer vision techniques. The goal is to enhance the quality of vintage images, remove noise, and reconstruct missing details to create high-resolution digital versions.

## Project Impact
This project not only contributes to preserving cultural and personal histories by digitizing old photographs but also showcases the effectiveness of traditional computer vision techniques in image restoration. The skills acquired during this project can be applied to various domains involving image enhancement and restoration.

## Methodology and Implementations

1.	Image Denoising
Performed image denoising by using fastN1MeanDenoising - searched for all the pixels that really resemble the pixel one wants to denoise. Denoising was then done by computing the average color of these most resembling pixels. The resemblance was evaluated by comparing a whole window around each pixel, and not just the color.

2.	Edge detection
Performed edge detection using Sobel Filter to detect scratches. This was not able to give good contours and, thus, implemented Canny Edge Detection to create closed contours and bounding boxes.

3.	Filtering out Scratches
Implemented a technique to distinguish contours associated with scratches from non-scratch ones. The technique relied on the intuition that the pixel intensity distribution of scratches has a small variance.

4.	Creation of Binary Scratch Mask
Did morphological closing to fill in the regions bounded by the contours.

5.	Image Reconstruction
Implemented a hybrid technique of Gaussian Pyramid and Telea algorithm to inpaint the scratches.

6.	Image Enhancement
Enhanced the reconstructed image using CLAHE for improved visual quality.



## References
1. [Bringing Old Photos Back to Life](https://doi.org/10.48550/arXiv.2004.09484)
2. [Detection and Removal of Scratches in Images](https://doi.org/10.1007/978-3-319-03844-5_22)


