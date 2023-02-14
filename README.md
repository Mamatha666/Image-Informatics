# Image-Informatics
#Denoising images

![image](https://user-images.githubusercontent.com/75186414/218887270-fe280d48-23b9-4b9a-a4d7-101cc8106e87.png)


2.1Steps of the Denoising algorithm:

1. Split the image into its Red, Green, and Blue (RGB) channels.
2. Analyze the histograms of the RGB channels to identify which channels have the most
noise.
3. Convert the image to the frequency domain using the FFT (Fast Fourier Transform)
algorithm.
4. Apply a low-pass filter (LPF) to the frequency domain image to remove high-frequency
noise. This can be done by setting the high-frequency coefficients in the frequency domain
image to zero.
5. Use the inverse FFT (IFFT) to convert the filtered frequency domain image back to the
spatial domain.
6. Apply a bilateral filter to the spatial domain image to further denoise the image while
preserving edges. The bilateral filter uses a Gaussian kernel to weight the pixels in the image,
with larger weights given to pixels that are close in color and spatial distance.
7. Repeat steps 1-4 for multiple iterations to achieve the desired level of denoising.
8. Evaluate images using SSIM and MSE metrics.
