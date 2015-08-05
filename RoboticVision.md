<link rel="stylesheet" href="css/theme/white.css" id="theme">

<!--section data-background-video="video.mp4,video.webm"-->

<div id="container">
  <div id="left" align="left"><img src="images/bot.gif" alt="bot" width="230" height="450" align="left"/></div>
  <div id="right">

	<table>
		<tr><td><img src="images/logo.jpg" alt="logo" width="110" height="110" /></td></tr>
		<tr><td><h5>Guru Nanak Dev Engineering College<h5></td></tr>
		<tr><td><h6>Ludhiana, Punjab, India</h6></td></tr>
		<tr><td><h2>SPATIAL OPERATORS</h2></td></tr>
	</table>

  </div>
</div>

---

# <h2>Spatial Operators</h2>

---

# <h2>Monadic Processing</h2>

* Each output pixel is a function of the corresponding input pixel
* The function is <span style="color:red">the same</span> for all pixels

---

# <h2>Spatial Operators</h2>

* The function can capture something about the <strong>uniformity</strong> or <b>variation</b> over the local pixel <strong>window</strong> W

---

# <h2>f(.) is an average</h2> 

* The average over the window
  - can reduce noise
  - reduces the resolution

---

# <h2>Moving Window Processes</h2>

---

# <h2>Effect of Window Size</h2>

* Features smaller than the window size will be strongly attenuated
  - we say the image is blurry, fuzzy, lower resolution etc.

---

> Code screenshots
Note: speaker notes FTW!

---

# Moving Window Issues

----

# <h2>The edge problem</h2>

* Some solutions:
  - don'<!--'-->t compute the output value when the window "falls off the edge"
  - assume the image is surrounded by zero pixels
  - assume the edge pixels are replicated outward

----

> code

----

# <h2>Window size is always odd</h2>

* The window is:
  - square
  - always centred on the input pixel
  - edge is integer <i>h</i> pixels from the centre
* The window width is <i>2h + 1</i>
  - always odd

---

# Introducing Kernels

----

# <h2>Artefacts of averaging</h2>

* Can lead to ringing
  - faint vertical & horizontal lines are introduced

----

# <h2>Averaging over a square is not isotropic</h2>

* Not all values used in the average are the same distance away
  - Undue influence by distant values

----

# <h2>Going isotropic</h2>

* Ideally we'<!--'-->d like to extract a circular region
  - but that would involve taking fractions of pixels

----

# <h2>Apply a weighting</h2>

* Circle of diameter 2.5 pixels

----

# <h2>Weighted kernel</h2>

----

# <h2>Scaling the kernel</h2>

* The scale factor is 
  - Typically make S = 1 to keep grey levels the same as the input image

----

# <h2>Simple averaging is also a kernel</h2>

----

# <h2>Gaussian kernel</h2>

----

# <h2>Gaussian width</h2>

* Choose the size of the square kernel to fit the Gaussian
* Rule of thumb h=3sigma

----

>code

---

# <h2>Correlation and Convolution</h2>

----

# <h2>Applying the kernel</h2>

* This is the definition of 2-dimensional <b>correlation</b>

----

# <h2>2D convolution</h2>

* Correlation is closely related to <span style="color:red">convolution</span>
   ????
* Convolution is <b>the same as correlation if the kernel is symmetric
* Often written in operator form ????

----

# <h2>Properties of convolution

* Commutative
  ???
* Associative
  ???
* Distributive
  ???
* Linear
  ???

----

# <h2>Advantages of associativity</h2>

* Convolving an image with a Gaussian kernel twice
  ???
* Is the same as convolving the image with a kernel that is the Gaussian convolved with itself

---

# Edges

----

# <h2> The intensity function</h2>

----

# <h2>Expressed as correlation with a kernel</h2>

----

# <h2>Convolution for edge detection</h2>

----

# <h2>Horizontal gradient image</h2>

----

# <h2>Vertical gradient as correlation with a kernel</h2>

----

# <h2>Vertical gradient image</h2>

----

# <h2>The Sobel kernel</h2>

----

# <h2>Sobel edge operator</h2>

----

# <h2>Image gradient direction</h2>

----

# <h2>Sobel Edge operator</h2>

---

# Kernels

----

# <h2>Gaussian kernel</h2>

----

# <h2>Derivative with smoothing</h2>

* Convolve image with the derivative kernel D
* If we smooth the image then ???

----

# <h2>Second Derivative</h2>

* The Laplacian is an isotropic second derivative
  - gives the gradient maxima in both the u- and v- directions

----

# <h2>Second derivative with smoothing</h2>

---

# <h2>Template matching</h2>

----

### image

----

### image2

----

### Spatial operators

----

### Tempate matching

* image
* image2

----

### Image Similarity

----

### picture

----

> code

---

## Rank Filtering

----

# <h2>Image noise removal</h2>

----

### Rank filtering

* image

----

### Image noise removal
* output image

---

# <h2>Mathematical Morphology</h2>

----

### image 1
* Morphology is about shape
* Output image contains shapes <b>compatible</b> with a structuring element S

----

# <h2>Erosion</h2>

* Output is true if all pixels in S are true (white)

----

# <h2>Dilation</h2>

* Output is true if any pixels in S are true (white)

----

# <h2>Erode then dilate</h2>

* Opening operation
* Only compatible shapes remain

----

# <h2>Dilation then Erosion</h2>

* Closing Operation

----

# <h2>Compatible structuring elements</h2>

--- 

## Lecture 5

