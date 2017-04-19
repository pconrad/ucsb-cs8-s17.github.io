---
layout: lab
num: lab02
ready: true
desc: "Lab02 - Using the Turtle Module and Writing Simple Functions"
assigned: 2017-04-19 08:00:00.00-7
due: 2017-04-21 23:59:59.00-7
---

<h1>Lab02: Using the Turtle Module and Writing Simple Functions in Python</h1>
<hr>
 <h2>Goals for this lab</h2>
 <p>By the time you have completed this lab, you should be able to: </p>
 <ul>
   <li>write simple functions to draw geometric shapes with Turtle Graphics</li>
   <li>test out these functions</li>
   <li>use IDLE to write and test programs</li>
   <li>write proper comments for your source code</li>
</ul>

 <h2>Step by Step Instructions</h2>
 <h3>Step 0: Get together with the lab partner you were assigned last week</h3>
   <p>If your partner is not present at the start of lab, please wait for five minutes and
   then ask the TA to pair you with someone else for this week.</p>
 <h3>Step 1: Be sure you are using a system that can show turtle graphics</h3>
 <ul>
   <li>Nothing to worry about if you are working <em>in</em> Phelps 3525 (as we hope) or CSIL.</li>
   <li>But you probably cannot show graphics by a remote connection via ssh to the lab
   computers. There are ways to do that, but learning them just for this lab is a waste of time.</li>
 </ul>
 <p>For the rest of these instructions, we are going to assume you are working in Phelps 3525 or CSIL.
    If not, you will need to adapt the instructions to your computing environment.</p>

 <h3>Step 2: Log in, create a lab02 directory, and open IDLE</h3>
 <p>Decide which one of you will be the first pilot for this lab, and then log in to the
    pilot's account and create a directory called lab02 inside his/her cs8 folder.
    You will work in this account for the rest of the lab, but remember to switch roles
    a couple of times between pilot and navigator during the course of the lab.</p>
 <p>By the way, there are two ways to create a new directory (folder):</p>
 <ul>
   <li>'One is to use a terminal window, and the <code>cd</code> and <code>mkdir</code>
   commands like you did in prior labs, <em>or</em></li>
   <li>Use the graphical user interface&mdash;pointing and clicking&mdash;to create a
   new folder.</li>
 </ul>

 <h3>Step 3: Open a &quot;New Window&quot; for function definitions</h3>
 <p>Next, in IDLE, select &quot;File=&gt;New Window&quot; to open a new &quot;untitled&quot; window for Python code
    (just like you did in lab00 for zen.txt).</p>
 <p>When it comes up, click and drag the window by its title bar over to the right of
    your Python Shell window (so the shell window is not covered up).</p>
<p>Once you have opened that file, add a comment to the top of your (Untitled) file like this one,
substituting your own name(s) and the current date in the proper spots:</p>
<pre># lab02.py
# Name: Agnes Nitt and Jason Ogg, 1/20/2015
# some functions to draw pictures using Turtle Graphics</pre>
<p>Then, save it under the name lab02.py inside your lab02 directory.</p>

<h3>Step 4. Getting Started with pat, the (<u>p</u>erfectly <u>a</u>dorable) <u>t</u>urtle</h3>
<p>First make sure that you can show turtle graphics. Try this command at the Python shell prompt
   (&gt;&gt;&gt;):</p>
<pre>&gt;&gt;&gt; import turtle<br>&gt;&gt;&gt; </pre>
<p>If what you get back is just another Python prompt (not a bunch of error messages) then you are good to go.</p>
<p>Then type (still in the Python shell window) the following command:</p>
<pre>&gt;&gt;&gt; pat = turtle.Turtle(&quot;turtle&quot;)</pre>
<p>That last command will open another new window - probably titled "Python Turtle Graphics" -
   and eventually this window will display your drawings. But ignore it for now. In fact, you
   will need to recreate it later.</p>
<p>Back in the new file window (lab02.py file), type the drawRectangle function
   that we did together in class and add a comment in front of it, as in the example below:</p>
  <pre class="codes"># function to draw a rectangle
# parameters: name of a turtle, and the width and height to draw
# draws: a rectangle at the position of the turtle</pre>
<p>Once you have typed in the function, save the file, and use the Run=&gt;Run Module
   command to &quot;compile&quot; your Python code. You might get an error message
   when you do this the first time - read the message, and figure out what to fix in
   your function definition. Keep fixing, saving and running the module until it
   works without error messages. Then look in the Python Shell window
   - you should see something like this:</p>
<pre>&gt;&gt;&gt; ================================ RESTART ================================<br>&gt;&gt;&gt;   
</pre>
<p>Congratulations! You just compiled and loaded into memory a useful function that we
   can use to make drawings.</p>
<p>Unfortunately though, IDLE just destroyed a portion of the work you did earlier:
   pat the turtle is gone from memory (the Python shell was restarted). Not such a big
   loss this time - just two commands to repeat, but annoying nonetheless. Thankfully IDLE
   does provide a way to repeat prior commands. Try that way now: click (with the mouse)
   on the "import turtle" line (inside the Python Shell window) and then hit the enter
   key - notice the command appears at the &gt;&gt;&gt; prompt - hit enter one more time
   to, well, enter it. Repeat the "pat = ..." command too.</p>
<p>Now, to test your function, try calling it with various values for width and height:</p>
<pre>&gt;&gt;&gt; drawRectangle(pat, 20, 50)
&gt;&gt;&gt; drawRectangle(pat, 100, 75)</pre>
<p>You can also try moving pat between the rectangles, picking up the pen first&mdash;for
   example this will move pat over a bit before drawing the next rectangle.</p>
<pre>&gt;&gt;&gt; pat.up()
&gt;&gt;&gt; pat.forward(100)
&gt;&gt;&gt; pat.down()
&gt;&gt;&gt; drawRectangle(pat, 60, 80)</pre>
<p>After playing with pat and the drawRectangle function for awhile, move on to Step 5.</p>

<h3>Step 5: Write a function to draw a house</h3>
<!-- 
<blockquote>
   IMPORTANT: You must try this step, but you do not have to succeed at it to earn full
   credit. Please begin it and try to finish it, but if you are running out of time before
   lab ends, then move on to Step 6 - the TA will check off your work even if it is not
   exactly correct, as long as you can show evidence that you tried.
</blockquote>
-->
<p><b>First switch roles between pilot and navigator if you did not already do that.</b></p>
<p>Add a function named drawHouse to the lab02.py file according to the following specifications:</p>
   <ol>
   <li>Add a couple of blank lines after the end of your drawRectangle function definition.</li>
   <li>The new function header must name two parameters: a turtle, and a width.</li>
   <li>Precede the header with an appropriate comment like you did for drawRectangle.</li>
   <li>The function body should use the turtle parameter to draw a house - make the
     height of the house proportional to its width. <i>Use the
     drawRectangle function</i> to make part of the house - <em>abstraction is good!</em></li>
   </ol>
   It should work correctly if used as follows:</p>
<pre>&gt;&gt;&gt; drawHouse(pat, 100)    # a really big house
&gt;&gt;&gt; drawHouse(pat, 10)     # a tiny house (just 10 pixels wide)</pre>
<table border="0"><tr>
  <td width="50%">Here is an example:<img align="center" src="house.png" alt="House" width="200"></td>
  <td align="left">Note: your house does not have to look exactly like this&mdash;i.e. the proportions of the
      width/height and the steepness of the roof can be different. As long as it &quot;looks like
      a house&quot;, that's good enough for this lab.</td>
</tr></table>

<h3>Step 6: Show off your work and get credit for the lab</h3>
<table bgcolor="yellow" border="1" cellpadding="4"><tbody><tr><td>
   Get your TA's attention to inspect your work, and to record your lab completion.
</td></tr></tbody></table>

<p><b>Don't leave early though ... see challenge problems below.</b></p>

<blockquote>
<h4>Step 6. Turning in your lab.</h4>
<p> You MUST have both your name and your partner's name in the file in order to receive
credit. Remember that the original pilot needs to do this step, since that is whose
account you have been using in Phelps 3525. Use the following command after you
cd into your cs8/lab02 directory:</p>
<pre>turnin Lab02@cs8 lab02.py</pre>
<p>After answering the questions, be sure to <em>wait for the message indicating success.</em></p>
</blockquote>

<hr>

<h2>Evaluation and Grading</h2>
Each student must accomplish the following to earn full credit for this lab:
<ul>
   <li>lab02.py is saved in original pilot's ~/cs8/lab02/ directory.</li>
   <li>lab02.py contains a working drawRectangle function, evidence of some attempt
       to write a drawHouse function, and all of the required comments.</li>
   <li>lab02.py has been turned in.
      <br><b>Deadline for after-lab submission: Friday at 11:59pm.</b>
      <br><i>Note that to be eligible for late turn-in with credit, you MUST have attended
          your entire lab period.</i></li>
   <li>If a pair completes the above tasks early, they <em>must</em> work the entire lab
    period by attempting extra challenge problems below.</li>
</ul>

<hr>

<blockquote>
<h3>Optional Extra Challenge</h3>
<ul>
<li>Make a function to draw a block (row) of houses.
    Precede the function definition with an appropriate comment, like always!
    Write the function header to take three
    parameters: a turtle, the width of one house, and the number of houses to draw:
    <pre>def drawBlock(turtle, width, number):</pre>
    <p>The function should draw as many houses as the parameter named number specifies,
    and each house should have the specified width. Separate the houses by moving the
    turtle without drawing any lines - pick up the pen, move, and then put it down again.
    We separate the houses in our solution by 1/2 house width. Here is an example
    (12 houses, each width 25 in the original drawing):</p>
    <p><img src="12houses.png" alt="row of houses"></p></li>
<li>Add a door and window(s) to your house, by modifying your drawHouse function. Of course
    you should use drawRectangle to help. Maybe add a chimney, eaves on the roof
    (by adjusting to let it overhang the sides), and/or other interesting features. After
    you test the new drawHouse function, and if you used it in your drawBlock function,
    then try drawBlock again to see your new features in a whole row of houses.</li>
<li>It should not be too difficult for you now to create a picketFence function - each
    slat of the fence is like a tall, skinny (plain) house, and a section of these slats
    is like a row of houses.</li>
<li>Still have time after writing picketFence? Then why not try a drawYard
    function that draws a house with a picket fence in front of it? You might even try
    to add a driveway, and a garage, and ...</li>
</ul>
</blockquote>
<hr>
 <p>Template & copy; 2009, Phillip T. Conrad, CS Dept, UC Santa Barbara. Permission to copy for non-commercial, non-profit, educational purposes granted, provided appropriate credit is given;  all other rights reserved. Adapted by Diana Franklin, Michael Costanzo, and Ziad Matni.</p>
