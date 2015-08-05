<link rel="stylesheet" href="css/theme/white.css" id="theme">

<!--section data-background-video="video.mp4,video.webm"-->

<div id="container">
  <div id="left" align="left"><img src="images/bot.gif" alt="bot" width="230" height="450" align="left"/></div>
  <div id="right">

	<table>
		<tr><td><img src="images/logo.jpg" alt="logo" width="130" height="130" /></td></tr>
		<tr><td><h5>Guru Nanak Dev Engineering College<h5></td></tr>
		<tr><td><h6>Ludhiana, Punjab, India</h6></td></tr>
		<tr><td><h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />SPATIAL OPERATORS</h2></td></tr>
	</table>

  </div>
</div>

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Monadic Processing</h2>

* Each output pixel is a function of the corresponding input pixel
* The function is <span style="color:red">the same</span> for all pixels

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Spatial Operators</h2>

* The function can capture something about the <strong>uniformity</strong> or <b>variation</b> over the local pixel <strong>window</strong> W

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />f(.) is an average</h2> 

* The average over the window
  - can reduce noise
  - reduces the resolution

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Moving Window Processes</h2>

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />ffect of Window Size</h2>

* Features smaller than the window size will be strongly attenuated
  - we say the image is blurry, fuzzy, lower resolution etc.

---

# 

> Code screenshots
Note: speaker notes FTW!

---

# Moving Window Issues

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />The edge problem</style>

* Some solutions:
  - don't compute the output value when the window "falls off the edge"
  - assume the image is surrounded by zero pixels
  - assume the edge pixels are replicated outward

---

> code

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Window size is always odd</h2>

* The window is:
  - square
  - always centred on the input pixel
  - edge is integer <i>h</i> pixels from the centre
* The window width is <i>2h + 1</i>
  - always odd

---

<!--'-->
# Introducing Kernels

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Artefacts of averaging</h2>

* Can lead to ringing
  - faint vertical & horizontal lines are introduced

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Averaging over a square is not isotropic</h2>

* Not all values used in the average are the same distance away
  - Undue influence by distant values

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Going isotropic</h2>

* Ideally we'd like to extract a circular region<!--'-->
  - but that would involve taking fractions of pixels

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Apply a weighting</h2>

* Circle of diameter 2.5 pixels

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Weighted kernel</h2>

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Scaling the kernel</h2>

* The scale factor is 
  - Typically make S = 1 to keep grey levels the same as the input image

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Simple averaging is also a kernel</h2>

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Gaussian kernel</h2>

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Gaussian width</h2>

* Choose the size of the square kernel to fit the Gaussian
* Rule of thumb h=3sigma

---

>code

---

# <h2 style="color:rgb(220,54,54); text-shadow: 2px 2px #000000" />Correlation and Convolution</h2>

---


