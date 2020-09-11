# Template-Matching-using-Cross-Correlation-OpenCV

<body style="">
<center>
<a href="http://www.bu.edu/"><img border="0" src="http://www.cs.bu.edu/fac/betke/images/bu-logo.gif" width="119" height="120"></a>
</center>

 Shoumik Majumdar<br>
 Team-mate: Tushar Sharma<br>
 <!--Your teammate names if applicable <br>-->
Feb 12, 2020
</p>

<div class="main-body">
<hr>
<h2> Problem Definition </h2>
<p> Using Template Matching and other basic computer vision techiniques to build a program using OpenCV that can
 recongnize 4 different hand shapes in real-time. </p>

<hr>
<h2> Method and Implementation </h2>
<p>Steps:</p>
<ol>
<li>Using background subtraction to make the program invariant to background noise</li>
<li>Detecting skin color by using a range of RGB values obtained through experiments </li>
<li>Using thresholding to binarize the image for detected skin pixels</li>
<li>Applied the same set of transformations to the template image</li>
<li>A range of scaling factors is used to scale the set of template images and it's compared with the source frame</li>
<li>The template with the highest NCC with the scene is reported</li>
<p>
Following OpenCV methods were used:
<ul>
<li>minMaxLoc: to find the maximum value (and its index)of a matrix </li>
<li>threshold: to binarize an image with a given threshold</li>
<li>rectangle, putText: to draw bounding box over the detected gesture</li>
<li>matchTemplate: to calculate the cross-correlation of two images</li>
</ul>
</p>

<hr>
<h2>Experiments</h2>
<p>These are the four different templates used: </p>
<table border=1>
<tr><th>Name</th><th>Template</th></tr>
<tr><td>Palm</td><td><img src="palm.jpeg" width="100" alt="Palm Template" >
<tr><td>Gun</td><td><img src="gun.jpeg" width="100" alt="Hole Template" >
<tr><td>L</td><td><img src="L.jpeg" width="100" alt="Peace Template" >
<tr><td>Peace</td><td><img src="peace.jpeg" width="100" alt="ThumbUp Template" >
</table>

<hr>
<h2> Results</h2>
<p>Here are several recognition results of all four hand shapes:</p>
<table border="1">
<tr><th>Hand Shape Name</th><th>Result</th></tr>
<tr><td>Palm</td><td><img src="palm-detected.jpeg" width="400" alt="Recongnition of a palm"></td></tr>
<tr><td>Gun</td><td><img src="gun-detected.jpeg" width="400" alt="Recongnition of a hole-shaped hand"></td></tr>
<tr><td>L</td><td><img src="L-detected.jpeg" width="400" alt="Recongnition of a V-shaped hand"></td></tr>
<tr><td>Peace</td><td><img src="peace-detected.jpeg" width="400" alt="Recongnition of a thumb-up"></td></tr>
</table>


<p>The following confusion matrix was obtained by changing the hand gestures </p>
<table border="1">
<tr><th>Hand Shape</th><th>Palm</th><th>Gun</th><th>L</th><th>Peace</th></tr>
<tr><th>Palm</th><td>6</td><td>0</td><td>0</td><td>1</td></tr>
<tr><th>Gun</th><td>0</td><td>6</td><td>0</td><td>0</td></tr>
<tr><th>L</th><td>0</td><td>2</td><td>5</td><td>2</td></tr>
<tr><th>Peace</th><td>2</td><td>0</td><td>1</td><td>5</td></tr>
<table>

<hr>
<h2> Discussion </h2>

<ul>
<li>As per our experiments, better accuracy was obtained when the background was plain.</li>
<li>Similar gestures like peace and palm were mistakenly recognized sometimes.</li>
<li>Rather than looping through different scaling factors for matching the template, we can extract the area of the palm and scale the template accordingly to make the program run much faster.</li>

</ul>
<p></p>

<hr>
<h2> Conclusions </h2>

<p>
Based on the discussion, we concluded that background subtraction is a powerful technique for isolating hand-motion and when coupled with thresholding, it becomes a useful tool for recognising different hand-gestures.
</p>


<hr>
<h2> Credits and Bibliography </h2>
<p>
https://docs.opencv.org/3.4/d1/dc5/tutorial_background_subtraction.html
</p>
<hr>
</div>

</body></html>
