# computer_vision
image_processing,CV2<br>
![cv](https://user-images.githubusercontent.com/89722385/134866233-d696455b-6722-4931-a601-d9a66193f7bd.jpg)


<b>Basic Image Processing Algorithms:<br></b>

In order for a computer to understand an image, the image has to be processed first. There are many algorithms that can be used to process images and the output depends on the task at hand.
Some of the most basic algorithms are:<br>
• Thresholding<br>
• Morphological transformations<br>
• Blurring<br>



Thresholding

Thresholding is commonly used to simplify how an image is visualized by both the computer and the user in order to make analysis easier. It is based on a value that the user sets and every pixel is converted to white or black depending on whether the value of every pixel is higher or lower than the set value. If the image is in grayscale, the output image will be white and black, but if you choose to keep the RGB format for your image, the threshold will be applied for every channel, which means it will still output a colored image.

1.Simple Thresholding:

If the pixel value is lower than the threshold set by the user, this pixel will be assigned a 0 value (black), or 255 (white). There are also different styles of thresholding within simple thresholding:
a).Threshold binary
b).Threshold binary inverted
c).Truncate
d).Threshold to zero
e).Threshold to zero inverted

Screenshot%20from%202021-09-23%2012-34-39.png

Threshold binary inverted works like binary but the pixels that were black are white and vice versa. Global thresholding is another name given to binary thresholding under simple thresholding.
Truncate shows the exact value of the threshold if the pixel is above the threshold and the pixel value.
Threshold to zero outputs the pixel value (which is the actual value of the pixel) if the pixel value is above the threshold value, otherwise it will output a black image, whereas threshold to zero inverted does the exact opposite.

2.Adaptive Thresholding:
Simple thresholding uses a global value as the threshold. If the image has different lighting conditions in some parts, the algorithm does not perform that well. In such cases, adaptive thresholding automatically guesses different threshold values for different regions within the image, giving us a better overall result with varying lighting conditions. There are two types of adaptive thresholding:

a).Adaptive mean thresholding
b).Adaptive Gaussian thresholding

The difference between the adaptive thresholding and simple thresholding is shown in below figure

adaptive.png

In adaptive mean thresholding, the threshold value is the mean of the neighborhood area, while in adaptive Gaussian thresholding, the threshold value is the weighted sum of the neighborhood values where weights are a Gaussian window.

3.Otsu's Binarization:
In global thresholding, we used an arbitrary value to assign a threshold value. Consider a bimodal image (an image where the pixels are distributed over two dominant regions). How would you choose the correct value? Otsu's binarization automatically calculates a threshold value from the image histogram for a bimodal image. An image histogram is a type of histogram that acts as a graphical representation of the tonal distribution in a digital image:

otsus.png



