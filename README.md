# ece253-homework-3-solved
**TO GET THIS SOLUTION VISIT:** [ECE253 Homework 3 Solved](https://www.ankitcodinghub.com/product/ece253-homework-3-solved-2/)


---

📩 **If you need this solution or have special requests:** **Email:** ankitcoding@gmail.com  
📱 **WhatsApp:** +1 419 877 7882  
📄 **Get a quote instantly using this form:** [Ask Homework Questions](https://www.ankitcodinghub.com/services/ask-homework-questions/)

*We deliver fast, professional, and affordable academic help.*

---

<h2>Description</h2>



<div class="kk-star-ratings kksr-auto kksr-align-center kksr-valign-top" data-payload="{&quot;align&quot;:&quot;center&quot;,&quot;id&quot;:&quot;92179&quot;,&quot;slug&quot;:&quot;default&quot;,&quot;valign&quot;:&quot;top&quot;,&quot;ignore&quot;:&quot;&quot;,&quot;reference&quot;:&quot;auto&quot;,&quot;class&quot;:&quot;&quot;,&quot;count&quot;:&quot;1&quot;,&quot;legendonly&quot;:&quot;&quot;,&quot;readonly&quot;:&quot;&quot;,&quot;score&quot;:&quot;5&quot;,&quot;starsonly&quot;:&quot;&quot;,&quot;best&quot;:&quot;5&quot;,&quot;gap&quot;:&quot;4&quot;,&quot;greet&quot;:&quot;Rate this product&quot;,&quot;legend&quot;:&quot;5\/5 - (1 vote)&quot;,&quot;size&quot;:&quot;24&quot;,&quot;title&quot;:&quot;ECE253 Homework 3 Solved&quot;,&quot;width&quot;:&quot;138&quot;,&quot;_legend&quot;:&quot;{score}\/{best} - ({count} {votes})&quot;,&quot;font_factor&quot;:&quot;1.25&quot;}">

<div class="kksr-stars">

<div class="kksr-stars-inactive">
            <div class="kksr-star" data-star="1" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="2" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="3" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="4" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" data-star="5" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>

<div class="kksr-stars-active" style="width: 138px;">
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
            <div class="kksr-star" style="padding-right: 4px">


<div class="kksr-icon" style="width: 24px; height: 24px;"></div>
        </div>
    </div>
</div>


<div class="kksr-legend" style="font-size: 19.2px;">
            5/5 - (1 vote)    </div>
    </div>
<div class="page" title="Page 2">
<div class="layoutArea">
<div class="column">
Problem 1. Canny Edge Detection

In this problem, you are required to write a function that performs Canny Edge Detection. The

function has the following specifications:

• It takes in two inputs: a grayscale image, and a threshold te. • It returns the edge image.

• You are allowed the use of loops.

A brief description of the algorithm is given below. Make sure your function reproduces the each step as given.

<ol>
<li>Smoothing: It is inevitable that all images taken from a camera will contain some amount of noise. To prevent noise from being mistaken for edges, noise must be reduced. Therefore the image is first smoothed by applying a Gaussian filter. A Gaussian kernel with standard deviation σ = 1.4 (shown below) is to be used.
2 4 5 4 2 1 4 9 12 9 4 k=159·5 12 15 12 5 4 9 12 9 4

24542
</li>
<li>Finding Gradients The next step is to find the horizontal and vertical gradients of the smoothed image using the Sobel operators. The gradient images in the x and y-direction, Gx and Gy are found by applying the kernels kx and ky given below:
−1 0 1 −1 −2 −1 kx=−2 0 2,ky=0 0 0.

−101 121 The corresponding gradient magnitude image is computed using:

| G | = 􏰕 G 2x + G 2y , and the edge direction image is calculated as follows:

Gθ = arctan( Gy ). Gx
</li>
<li>Non-maximum Suppression (NMS): The purpose of this step is to convert the thick edges in the gradient magnitude image to “sharp” edges. This is done by preserving all local maxima in the gradient image, and deleting everything else. This is carried out by recursively performing the following steps for each pixel in the gradient image:
• Round the gradient direction θ to nearest 45◦, corresponding to the use of an 8-connected neighbourhood.
</li>
</ol>
</div>
</div>
<div class="layoutArea">
<div class="column">
2

</div>
</div>
</div>
<div class="page" title="Page 3">
<div class="layoutArea">
<div class="column">
<ul>
<li>Compare the edge strength of the current pixel with the edge strength of the pixel in the positive and negative gradient direction i.e. if the gradient direction is north (θ = 90◦), then compare with the pixels to the north and south.</li>
<li>If the edge strength of the current pixel is largest; preserve the value of the edge strength. If not, suppress (remove) the value.</li>
</ul>
4. Thresholding: The edge-pixels remaining after the NMS step are (still) marked with their strength. Many of these will probably be true edges in the image, but some may be caused by noise or color variations. The simplest way to remove these would be to use a threshold, so that only edges stronger than a certain value would be preserved. Use the input te to perform thresholding on the non-maximum suppressed magnitude image.

Evaluate your canny edge detection function on geisel.jpg for a suitable value of te that retains the structural edges, and removes the noisy ones.

Things to turn in:

<ul>
<li>The original gradient magnitude image, the image after NMS, and the final edge image after thresholding.</li>
<li>The value for te that you used to produce the final edge image.</li>
<li>Code for the function.
Problem 2. Butterworth Notch Reject Filtering in Frequency Domain

This problem will follow Figure 4.64 in section 4.10.2 Notch Filters of Gonzalez &amp; Woods 3rd

Edition.
</li>
</ul>
(i) Read in the image Car.tif, pad the image to 512×512 (using zero padding on all four sides of the image), and display the 2D-FFT log magnitude (after moving the DC component to the center with fftshift). Please refer to the links available here and here.

You should see symmetric “impulse-like” bursts which we suspect is the cause of the Moire Pattern (the dot pattern from the newspaper image). We would like to filter out this pattern in the frequency domain using a Butterworth Notch Reject Filter given by:

</div>
</div>
<div class="layoutArea">
<div class="column">
􏰔K􏰒 1 􏰓􏰒 1 􏰓

</div>
</div>
<div class="layoutArea">
<div class="column">
HNR(u, v) =

D−k(u, v) = 􏰐(u + uk)2 + (v + vk)2􏰑1/2 (3) 3

</div>
</div>
<div class="layoutArea">
<div class="column">
1 + [D0/Dk(u, v)]2n 1 + [D0/D−k(u, v)]2n (1) Dk(u, v) = 􏰐(u − uk)2 + (v − vk)2􏰑1/2 (2)

</div>
</div>
<div class="layoutArea">
<div class="column">
where

</div>
</div>
<div class="layoutArea">
<div class="column">
k=1

</div>
</div>
</div>
<div class="page" title="Page 4">
<div class="layoutArea">
<div class="column">
Here, we have slightly modified the definition from the textbook slightly in that we removed M/2 and N/2 from the equation so that the center of the DFT image is 0 rather than (M/2, N/2).

The parameter K is the number of “impulse-like” bursts you would like to remove (excluding their symmetric counterparts since the HNR equation already includes it), e.g. 4 for this image rather than 8. The parameters n and D0 are scalar values that you may choose to control the transition and radius of the notch filters. The parameter uk and vk is the location of the kth “impulse-like” bursts in the 2D DFT magnitude image. u and v are all possible (u,v) coordinate pairs that you want to generate HNR for:

<pre>     Python:
     x_axis = np.linspace(-256,255,512)
     y_axis = np.linspace(-256,255,512)
     [u,v] = np.meshgrid(x_axis,y_axis)
</pre>
(ii) Repeat for Street.png, except for K=2 and remove the burst along the u = 0 axis and the v = 0 axis.

Things to turn in:

<ul>
<li>All images should have colorbars next to them</li>
<li>All DFT magnitude images should have the DC frequencies in the center of the image</li>
<li>4 images from 2(i): 1 unpadded original image, the corresponding 2D DFT log-magnitude, the butterworth Notch Reject Filter in frequency domain HNR(u,v), the final filtered image</li>
<li>10 parameters for 2(i): n, D0, u1, v1, …, u4, v4</li>
<li>4 images from 2(ii): 1 unpadded original image, the corresponding 2D DFT log-magnitude,
the butterworth Notch Reject Filter in frequency domain HNR(u,v), the final filtered image
</li>
<li>6 parameters for 2(ii): n, D0, u1, v1, u2, v2</li>
<li>Code for 2(i), 2(ii)
Problem 3. PyTorch tutorial and questions

After seeing some awe-inspiring machine learning results, do you want to try some yourselves? Let’s start with some basic practice of machine learning framework: PyTorch. Please follow the tutorial for cifar10 classifier (cifar10 tutorial) and answer the following questions.

(i) Login to the server for CPU/GPU resources. (0 point)

• https://datahub.ucsd.edu/ (Jupyterhub)

• Select environment (with or without GPU. You don’t need GPUs in this homework.) • Launch environment.
</li>
</ul>
</div>
</div>
<div class="layoutArea">
<div class="column">
4

</div>
</div>
</div>
<div class="page" title="Page 5">
<div class="layoutArea">
<div class="column">
<ol start="2">
<li>(ii) &nbsp;How many images and batches are used to train the network?</li>
<li>(iii) &nbsp;Do we normalize the images? What do we do in the example?</li>
<li>(iv) &nbsp;The losses are dropping! Can you plot out the training loss?</li>
<li>(v) &nbsp;Now the network is done training. Can you check some successful cases and some failure cases (show some images classified by the network)?</li>
<li>(vi) &nbsp;Can you visualize the output of the 1st layer of CNN using one image from the training set?</li>
</ol>
References:

• deep learning 60min blitz • pytorch with examples

</div>
</div>
<div class="layoutArea">
<div class="column">
5

</div>
</div>
</div>
