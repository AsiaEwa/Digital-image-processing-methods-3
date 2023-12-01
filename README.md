# Digital-image-processing-methods-3
Digital image processing m
1. Transform the image to obtain an output image in shades of gray.
2. Display the histogram and align it
   The image can be normalized using a for loop (in the loop, the output image should be divided by the product of its width and height)
   
   ![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/fb1caa5c-599b-4d9c-a770-571b4dba7db7)
   
After equalizing the histogram, the following image and histogram were obtained:

   ![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/e104c2e1-c178-4998-b61c-49584873e51c)

After equalizing the histogram, the image gained greater contrast, became clearer and sharper. You can also notice more visible grain and noise in the photo. The image became more saturated. Before the change, it was brighter and more subdued than after equalization.

Script2 loads the Len image, converts it to a black and white image, determines the dimensions of the image by modifying them to the given ones, creates the image using the p factor, creates the necessary vectors, increases the occurrence of a given value in the black and white image, assigns the LUT values, then the LUT values black and white image.
During the operation, the histogram is equalized and the photo and histogram are displayed

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/07a0f456-c916-40f9-a741-9a1f0390af28)

-min IN = 0 Decreasing the minIN parameter brightens the image.
![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/ce029a81-f3ec-4eeb-8e2e-9e1ecf5a384f)
![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/40bce9b2-78c0-443e-a963-f6d2bf1aeec8)

  -minIN = 100 - minIN = 200 Increasing the minIN parameter darkens the image.
  
![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/7a71d77f-e7a4-4f84-9331-fc91b2776f39)

  -maxIN = 100

Decreasing the maxIN parameter increases the image contrast. The photo is bright, but dark parts are strongly highlighted.
-maxIN=150 The photo is sharpened but there is no strong contrast

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/2aa3385d-72c7-4a57-9390-4bde9cbc681f)

maxIN = 255 The photo is in a dark tone, which makes the black elements especially visible and the very bright ones a little less visible.

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/bfe53c9f-e189-49e7-b66f-fc54fdb91515)

Increasing the maxIN parameter reduces the image contrast.
-p = 0.1
 
![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/9046fbc5-4b05-495c-a3a4-b14b66d1a1bc)

Decreasing the p parameter darkens the image.
-p=0.65

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/97c0bbba-86e9-4fd4-93cf-6018463b3920)

- p = 0.9

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/f06a76b6-9bb8-428d-9cba-b7e6546e215f)

The parameter p =1 leaves the image unchanged
Analyzing the results, it can be noticed that in the case of a large range of parameters, the image is very close to the original one, because there is a wide gray scale. Narrowing the borders to intermediate values increases the contrast and extracts shadows from the image, making details more visible. If it narrows too much, a lot of information in the image is lost and the shade scale is very small. Narrowing strongly towards high values makes the image dark, there are many black areas. If you move towards the upper values, the image is bright, mainly white areas are visible, the rest is hidden.

Script 3 works as follows:
- takes an image and transforms it to shades of gray
- creates a histogram
- transforms the histogram into cumulative
- balances the histogram
- displays images and histograms

Grayscale image histogram:

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/554d3e8b-0ef0-48b7-9747-e290f20c67f6)

Cumulative histogram:

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/6906ddd4-fe38-4d60-8852-b66a28182585)

A non-uniform curve shows an increase in the number of samples with a given value. A straight line means there are no samples with a given value, and the steeper the curve, the greater the number of samples with a given value. A curve has been generated, so it can be concluded that the image does not have the same number of samples in each value.
Histogram after equalization:

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/f375e2e8-aa4c-4501-9479-090ebb039983)

Image after alignment:

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/d3288379-4f10-4e92-a447-5dcdd39a0f39)

The resulting image is clear, sharp, and has an equal proportion of light and dark pixels
Cumulative histogram after equalization:
The resulting image is clear, sharp, and has an equal proportion of light and dark pixels
Cumulative histogram after equalization:

![image](https://github.com/AsiaEwa/Digital-image-processing-methods-3/assets/101841759/e8a5513a-3d0a-469d-8b62-9aa89d00d424)

The cumulative histogram after equalization is a straight line with a given slope. (No increases or decreases are visible.) This means that there are equal samples of a given value in the image and the image alignment process was successful.
