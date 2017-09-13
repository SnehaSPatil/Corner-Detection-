# Corner-Detection-
Steps for Corner Detection 
1) Filtering 
Gaussian filtering is used to achieve smoothing and filtering. The Gaussian used is zero mean. The standard deviation was varied to note the effect. It was found that as we increase the value of standard deviation the edges and corner pixels blur, thus comparatively few corners are detected for the same value of other parameters. 
2) Creating a ‘C’ matrix and finding appropriate pixels based on Eigen values 
Using the image gradient values a symmetric matrix was created for each pixel using the neighbors depending on the given window size. Eigen values were found for each pixel. 
Selecting pixels with the proper Eigen values 
Corner pixels have λ1 > 0 and λ2> zero. Thus only pixel positions with such Eigen values were stored. The smallest of the Eigen value greater than threshold was stored. 
3) After sorting the repetitive corner points were removed and output image along with the marked corners was displayed A function called CornerDetection(sigma, A, neigh, Lth) was written which takes the source image ‘A’, standard deviation ‘sigma’ for the Gaussian filter, the low threshold ‘lth’ on the smaller Eigen value, and ‘neigh’ which is the number of neighbors on each side of the pixel to be considered. The total window size would be (2 * neigh + 1) 
