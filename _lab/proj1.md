---
layout: lab
num: project1
ready: false
desc: ""
assigned: 2017-04-20 08:00:00.00-7
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
      When done, your results should match the following sample runs from our solution.
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
  every number after the first two is the sum of the two preceding ones, so the sequence starts with a 0 and 1 
  and continues on. This gives us this series of numbers: 0 1 1 2 3 5 8 13 21 34 55… etc…
  Write a Python program that prints out the first n numbers in the Fibonacci Series. Do not copy a solution from 
  an online source. You cannot recursively call the function and can only use if/else and for statements.
     <dl><dd><code>fibo(n)</code> - where n is the number of terms in the series.</dd></dl>

<ul type="circle">
     <li>If n is equal to 0, then just include the first term in the equation: <code>(1)</code>.
         If n is equal to 1, then just include the first and the second term in the equation: <code>(1 1)</code>.
         If n is equal to 6, include the first six terms: <code>(1 1 2 3 5 8)</code>
     </li>
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
  	<li>(25 points: string manipulation) Write 2 functions that do the following:
  	<p>FindWords(lines, word) takes in a group of lines (called a <b>list</b>) 
	and goes through each line and searches for the word in string "word". If it finds 
	the word, it prints the entire line, preceded by the line number (these start at 0).</p>
	
	<p>PrintBackwards(lines, n) takes in that same group of lines and asks the user 
	to pick a line number and then proceeds to print that line backwards.</p>

	<p>Both functions are to be part of the program readText.py, which reads in the entire 
	poem, "The Raven" by Edgar Allan Poe, saved in the file "theRaven.txt".</p>
    </li>
    <ul>
        <li>When a list contains multiple values, you can access each individual one with a for-loop, 
		for example, given a list called <code>many = ["joe", "mary", "bob", "chincilla"]</code>, you would do this: 
			<p><code>for one in many: </code></p>
			<p><code>...   print(one)</code></p>
			This will print out each name in the list individually, each on a new line.
       		<p>If you modify the last line as <code>print(one, end= " ")</code>, you will print each item 
			next to the following one on one line with a space character between each one.</p> 
        </li>
     <p>Here are some sample results from my solution:</p>
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
</ol>
</div>
