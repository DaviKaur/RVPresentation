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


