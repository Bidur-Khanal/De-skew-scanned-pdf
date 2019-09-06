## De-skew Scanned pdf ##

This repository includes basic python scripts to correct skewed pdf documents, written in ipynb notebooks.
Here, I have used two different approaches to de-skew pdf documents:

*Using Hough Line Transform
 > Here, I have used Hough Line Transform after OTSU binary thresholding for skewed angle detection.
Hough Line Transfrom is computationally sound and various libraries provide optimized functions to perform Hough Transform.
Finally, I corrected the image reversing the skewed angle.



*Using Fourier Transfrom + Hough Transform
 > Here, I first applied fourier transfrom to the image. In the Fourier domain image, each point represents a particular frequency contained in the spatial domain image.
Then I used edge detection to extract edge feature (which is usually like  white strip of light showing the orientation).
Last, I applied hough tansform to detect the line and its orientation and corrected it.
***

<p>
<img src="https://github.com/Bidur-Khanal/De-skew-scanned-pdf/blob/master/images/25.png" width="400" height="300"> 
<em>Original Image</em>
<img src="https://github.com/Bidur-Khanal/De-skew-scanned-pdf/blob/master/images/25%20corrected.png" width="400" height="300"> 
<em>De-skewed Image</em>
</p>
***
References:

https://homepages.inf.ed.ac.uk/rbf/HIPR2/fourier.htm
https://plus.maths.org/content/fourier-transforms-images
https://www.researchgate.net/publication/221472741_A_New_Algorithm_for_Skew_Detection_in_Images_of_Documents
https://www.researchgate.net/publication/295256106_An_approach_for_Skew_Detection_using_Hough_Transform 
https://www.researchgate.net/publication/287217803_A_Survey_on_Document_Image_Skew_Detection 
https://www.researchgate.net/publication/294578383_A_Novel_Skew_Detection_and_Correction_Approach_for_Scanned_Documents 
http://scikit-image.org/docs/dev/api/skimage.transform.html#skimage.transform.hough_line_peaks 
http://citeseerx.ist.psu.edu/viewdoc/download;jsessionid=52D3EF125E41240A6C364B2E32721F2B?doi=10.1.1.105.3741&rep=rep1&type=pdf
