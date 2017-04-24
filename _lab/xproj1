---
layout: lab
num: project1
ready: false
desc: ""
assigned: 2017-04-27 12:30:00.00-7
due: 2017-05-04 23:59:59.00-7
---
<div markdown="1">

<h1>CS 8, Spring 2016: Programming Project 1</h1>
<h2>Due: Thursday, XXXXXXX, 11:59pm</h2>

<strong>Before you begin:</strong>
Read all of Miller/Ranum chapters 1, 2 and 3 and obtain copies of these 4 files:
<ul>
    <li>sphere.py</li>
    <li>screensize.py</li>
    <li>fibonacci.py</li>
    <li>myText.py</li>
</ul>
	
The files are found on <code>~zmatni/cs8s17/projects/p1/</code>, and save
them in whatever folder you choose to work on this project (presumably <code>~/cs8/p1/</code>).
  
Edit the comments at the beginnings of these files to include your name (and the name of your partner, 
if you are working with another student) and the date each program is written.
This is IMPORTANT, and it applies to all future programs too!

<ol>

<hr>
<!-- PART 1-->
<h2>sphere.py</h2>
  <li>(25 points: some calculations) Add the following four functions to sphere.py (three of them are taken from
      Exercises 2.1, 2.2 and 2.3 on page 81 of the text, and the other is a natural addition):
    <ol type="a">
      <li><code>circumference(r)</code> - to return the circumference of a circle with radius
          <code>r</code>. [<code>2&pi;r</code>]</li>
      <li><code>area(r)</code> - to return the area of a circle with radius <code>r</code>.
          [<code>&pi;r<sup>2</sup></code>]</li>
      <li><code>surface(r)</code> - to return the surface area of a sphere with radius
          <code>r</code>. [<code>4&pi;r<sup>2</sup></code>]</li>
      <li><code>volume(r)</code> - to return the volume of a sphere with radius
          <code>r</code>. [<code>4&pi;r<sup>3</sup>/3</code>]</li>
    </ol>
    Notes:
    <ul type="circle">
      <li>The function headers must <em>exactly match</em> the ones above, or the testing code
          will not work.</li>
      <li>Use <code>math.pi</code> (after importing the math module) for the value of &pi; in all of
          these calculations.</li>
      <li>We suggest you test them one at a time in the Python shell. When they are all done, you
          can run the module. Here are two sample runs to which you can compare your results:
      <pre>-bash-4.2$ <b>python3 sphere.py</b> 
enter radius: <b>2.5</b>
circumference: 15.7
circle area: 19.6
sphere volume: 65.4
sphere surface area: 78.5
-bash-4.2$ <b>python3 sphere.py</b> 
enter radius: <b>10</b>
circumference: 62.8
circle area: 314.2
sphere volume: 4188.8
sphere surface area: 1256.6</pre></li>
    </ul>

<hr>
<!-- PART 2-->
<h2>screensize.py</h2>
  <li>(25 points: slightly more complicated calculations) Add two functions to screensize.py to calculate the height and width of a display
      screen, given the diagonal screen size (D) and the aspect ratio (W:H), using these formulas:
      <blockquote><table border="1" cellpadding="5"><tr>
      <td width="50%"><img src="heighteq.png"></td>
      <td width="50%"><img src="widtheq.png"></td>
      </tr></table></blockquote>
      <ol type="a">
        <li><code>height(D, W, H)</code> - where D, W and H are described above.</li>
        <li><code>width(W, H, screenHeight)</code> - where W and H as above, and screenHeight is the result of
           the height function.</li>
      </ol>

      <p>When done, your results should match the following sample runs from our solution.</p>
      <pre>-bash-4.2$ <b>python3 screensize.py</b> 
enter D, W, H (separated by commas): <b>51, 4, 3</b>
width = 40.8, height = 30.6
-bash-4.2$ <b>python3 screensize.py</b> 
enter D, W, H (separated by commas): <b>64, 16, 9</b>
width = 55.8, height = 31.4</pre></li>

<hr>
<!-- PART 3-->
<h2>fibonacci.py</h2>
  <li>(25 points: accumulator pattern) The numbers in the Fibonacci Series are characterized by the fact that 
  every number after the first two is the sum of the two preceding ones, so the sequence starts with a 1 and 1 
  and continues on. This gives us this series of numbers: 1 1 2 3 5 8 13 21 34 55… etc…
  <p>Write a Python program that prints out the first n numbers in the Fibonacci Series. Do not copy a solution from 
  an online source. You cannot recursively call the function and can only use <code>if/else</code> and <code>for</code> statements.</p>

<ul type="circle">
     <code>fibo(n)</code> - where n is the number of terms in the series.
	 <p>Examples:</p>
     <li>If n is equal to 1, then just include the first term in the equation: <code>(1)</code>.</li>
     <li>If n is equal to 2, then just include the first and the second term in the equation: <code>(1 1)</code>.</li>
     <li>If n is equal to 6, include the first six terms: <code>(1 1 2 3 5 8)</code></li>
     
     <li>When done, your results should match the following sample runs from our solution.
     <pre>
	-bash-4.2$ <strong>python3 fiboncci.py</strong> 
	enter number of terms: <b>9</b>
	1 1 2 3 5 8 13 21 34
	-bash-4.2$ <strong>python3 fibonacci.py</strong>
	enter number of terms: <b>1</b> 
	1
	-bash-4.2$ <strong>python3 fibonacci.py</strong>
	enter number of terms: <b>5</b>
	1 1 5 8 13
	-bash-4.2$ <strong>python3 fibonacci.py</strong>
	enter number of terms: <b>9</b>
	1 1 5 8 13 21 34 55 89
	</pre>
	</li>
</ul>

<hr>
<!-- PART 4-->
<h2>myText.py</h2>
  	<li>
	(25 points: string manipulation) This program calls TWO functions that manipulate strings. Both functions are 
	run over and over again until the user enters specific outputs to quit (see example below).
  	<p><code>FindWords(lines, word)</code> takes in a group of strings stored together (that is, lines in a <b>list</b>) 
	and goes through each string (line) in this list and searches for the sub-string "word". If it finds 
	"word", it prints the entire line, preceded by the line number (these start at 0). </p>
	<p>The line number is the position of the line in the list. So for example, if the list has 125 lines in it and the one indexed 
	number 103 is "found" by the function and is "Quoth the Raven "Nevermore"", then the function would output:</p>
	<pre>
	103             Quoth the Raven "Nevermore." 
	</pre>
	
	<p><code>PrintBackwards(lines, n)</code> takes in that same group of lines and asks the user 
	to pick a line number and then proceeds to print that line backwards. Using the same example as above, if 
	the user answer to the question is "103" (as in, line 103), then that line is printed backwards, like so:</p>
	<pre>
	".eromreveN" nevaR eht htouQ
	</pre>

	<p>Both functions are to be part of the program readText.py, which reads in the entire 
	poem, "The Raven" by Edgar Allan Poe, which is saved in the file "theRaven.txt" (the reading of the 
	file is done for you in the main program).</p>
    </li>

    <ul>
        <li>NOTE: When a list contains multiple values, you can access each individual one with a for-loop, 
		for example, given a list called <code>names = ["joe", "mary", "bob", "chincilla"]</code>, you would do this: 
			<pre>
			for one in names:
				print(one)
			</pre>
			This will print out each name in the list individually, each on a new line.
       		<p>If you modify the last line as <code>print(one, end= " ")</code> (note the space character between 
			the quotation marks), you will print each item next to the following one on one line with a 
			space character between each one. If you modify it further as <code>print(one, end= "")</code> (note 
			the ABSENCE of a space characer between the quotes), you will print each item immediately next to the other with 
			no space character between them.</p>
        </li>

     <p>When done, your results should match the following sample runs from our solution.</p>
	 <p><img src="readText.png" width="800"></p>
     </ul>

<hr>
  <li>Go to CSIL (in person unless you can manage this step remotely without any
      assistance from us). Open a terminal window, <code>cd</code> to the
      <em>same directory as your source code files</em>, then type the following (careful -
      turning in to uppercase P, Proj1, at class account cs8):
      <pre>turnin Proj1@cs8 sphere.py screensize.py fibonacci.py readText.py theRaven.txt</pre>
      If you are working with a partner, be sure that <em>both partners names</em> are in the
      comments at the top of all source files.</li>


