README FOR FEATURE EXTRACTION

This code is an example of image matching and stitching using the SIFT (Scale-Invariant Feature Transform) algorithm and RANSAC (Random Sample Consensus) for robust homography estimation. It demonstrates how to detect keypoints, compute descriptors, match keypoints, estimate homography, and stitch two images together.

Dependencies
- OpenCV (cv2)
- Numpy

Code Explanation
1. The code first loads the two input images and converts them to grayscale using the OpenCV library.
2. The SIFT object is created to detect keypoints and compute descriptors for each image.
3. Keypoints are drawn on the images using the `drawKeypoints()` function.
4. The keypoints are matched using the Brute-Force Matcher (`BFMatcher`).
5. RANSAC is applied to find the best homography between the keypoints using random samples.
6. Outliers are removed based on the homography.
7. The second image is warped using the best homography.
8. The two images are blended together using `addWeighted()` to create the final stitched image.
