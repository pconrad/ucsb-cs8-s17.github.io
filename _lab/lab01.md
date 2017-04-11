---
layout: lab
num: lab01
ready: false
desc: "Lab01 - Starting with Python and IDLE"
assigned: 2017-04-12 08:00:00.00-7
due: 2017-04-14 23:59:59.00-7
---

<h1>Lab01: Writing and Running Python code, Expressions, Pair Programming</h1>
<hr>
 <h2>Goals for this lab</h2>
 <p>By the time you have completed this lab, you should be able to </p>
 <ul>
   <li>Write and run Python code in IDLE</li>
   <li>Write expressions and assign values to variables in Python</li>
   <li>Perform drive and navigator roles of pair programming</li>
</ul>

<p>Watch this video about Pair Programming at <a href="http://cs.ucsb.edu/~mikec/pairvideo.html">http://cs.ucsb.edu/~mikec/pairvideo.html</a>.</p>
<p>Do not worry if this is your first experience with Pair Programming. You will learn more about it as the 
quarter progresses.  In short, there are two roles: pilot and navigator.
The pilot sits at the computer and types, and the navigator helps.  It is 
important that each of you thinks about the problems independently.  The
pilot directs, but does not leave the navigator behind.  The navigator
assists, but does not give the pilot commands. You are helping each other
so that you both understand the work.</p>

 <h2>Step by Step Instructions</h2>
 <h3 id="step1">Step 1: Choose initial pair programming roles</h3>
<p>Choose who will be the pilot for the first part 
of the lab.  The pilot should sit down in front of the computer now.
The navigator gets a chair and sits next to the pilot.</p>

  <h3>Step 2: Log in, create a lab01 directory, and open IDLE</h3>
<p>Log onto the pilot's account. If the pilot's account is not working, 
allow the navigator to log in instead.  
Navigate using "cd" to get to your cs8 directory, and use "mkdir" to create
a new directory lab01. Then navigate into the lab01 directory, and open IDLE:
<pre>-bash-4.2$ <b>cd cs8</b>
-bash-4.2$ <b>mkdir lab01</b>
-bash-4.2$ <b>cd lab01</b>
-bash-4.2$ <b>idle3</b></pre>
Leave the IDLE window open to use in later steps. But first some paper work to do.</p>

<h3>Step 3: Writing expressions in Python</h3>
<em>On a piece of paper</em>, write the following items as expressions in Python.
Make sure you construct your expressions so that the answer is the right <em>type</em>.
<ul> <li>
Calculate a student's GPA from last quarter. The student had four classes, all worth
four units, and received A-(3.7), B+(3.3), A(4.0), and A+(4.0).  
Write an expression - on paper - to calculate the GPA.
</li><li>
The Andromeda galaxy is 2.9 million light-years away.  There are 
5.878 * 10^12 miles per light-year. Write an expression to find out how many miles
away is the Andromeda galaxy? (Careful though: 10^12 means "10 to the 12th power"
but in Python, ^ is not the symbol used to raise a value to a power. Ask a TA if
you really can't remember the way to do it.)
</li><li>
Find the average age of you and your parents using floating-point division.
</li><li>
You save the water in the shower as it is warming up to water your plants.
Your container is a cube, 10 inches on a side.  The water fills up 5/6 of the 
container each time.  How much water, in mL, does your shower take to warm up?
FYI: 1 cubic inch equals 16.387064 mL.
</li></ul>

<p>Before moving on, make sure you and your partner have gone through the 
answers.  If you disagree on any, discuss why each of you thinks it should
be a particular way.  Do not worry if you do not come to any agreement right
now - you can try both ways and see who is right.  Just make sure that when
you do verify which is right, you both understand <em>why</em> that was the correct
answer.</p>

 <h3 id="step4">Step 4: Writing code in IDLE</h3>
<p>In IDLE, you have two choices for testing your expressions.  First, you may
write each one individually into the Python shell and see what the results
are.  This is useful for trying out something small, like the expressions
above.  So first try each of your answers out in the Python shell.
You can quickly check your work by doing this. For example (user input is bold):</p>
<pre>>>> <b>4 + 3 * 2</b>
10</pre>
<p>Often, though, it is useful to write the code and be able to execute
it several times without retyping the whole thing.  
As last time, select <u>File->New Window</u> to open a new window for Python code.
At the top of your file, write a Python comment (start it with a '#' character)
that includes both your name and your partner's name, as well as the current date.
For example:</p>
<pre># JoeBob Smith and SallyMay Johnson, 1/13/2015</pre>
<p>Save the file as you saw last time using <u>File->Save As</u>. Name it lab01.py
and save it in your lab01 directory.</p>
<p>Then type your expressions into the new window, but enclose each one in a
call to print(). The reason is that when
you run all of the expressions at once, Python executes them internally.
To see each result, you need to print the results of the expression.
For example, to evaluate the expression 4 + 3 * 2, type this code:
<pre>print(4 + 3 * 2)</pre>
<p>Select <u>Run->Run Module</u> to cause all of the Python code to execute, line-by-line.
Save when necessary.</p>

<h3>Step 5: Assigning Variables in IDLE</h3>
<p><font size="+1"><b>First: switch roles between pilot and navigator if you did not
already do that.</b></font><br>
The navigator is now at the keyboard and becomes the pilot.
The pilot becomes the navigator to assist the pilot.
<br>Always stay logged into the <em>original</em> pilot's account.</p>
<p>For each of the expressions in your file, decide on an appropriate variable name
and assign the result of the expression into the variable. Then in the print statements,
place the variable name rather than the expression. For example:</p>
<pre>answer = 4 + 3 * 2
print(answer)</pre>
<p>Rerun your module so that you can see the results.</p>
<p>Also, notice that after running the module, you can just type the variable name into the
Python shell to display the value. Try that with one or more of your variables.</p>

<h3>Step 6: Show off your work and get credit for the lab</h3>
<table bgcolor="yellow" border="1" cellpadding="4"><tbody><tr><td>
   Get your TA's attention to inspect your work, and to record your lab completion.
</td></tr></tbody></table>

<p>Don't leave early though ... see challenge problems below.</p>

<blockquote>
<h4>Step 6a. ONLY IF YOU RAN OUT OF TIME TO HAVE THE TA INSPECT YOUR WORK</h4>
<p>If you must complete this assignment at CSIL, then submit it with the
turnin program. You MUST have both your name and your partner's name in the 
file in order to receive credit. Remember that
the original pilot needs to do this step, since that is whose account you have 
been using in Phelps 3525.</p>
<p>Bring up a terminal window on CSIL, and cd into the original pilot's cs8
directory, and cd again into the lab01 directory. Then type the following:</p>
<pre>turnin Lab01@cs8 lab01.py</pre>
<p>Respond &quot;yes&quot; when the program asks if you want to turn in (be sure to read the
list of files you are turning in), and then <em>wait for the message indicating success.</em></p>
</blockquote>

<hr>

<h2>Evaluation and Grading</h2>
Each student must accomplish the following to earn full credit for this lab:
 <ul>
   <li>Turn in a complete and accurate Hw1.</li>
   <li>lab01.py is saved in original pilot's ~/cs8/lab01/ directory, and it works properly.</li>
   <li>ONLY IF STEP 6a IS NECESSARY - lab01.py has been turned in.
      <br><b>Deadline for after-lab submission: Tonight at 11:59pm.</b>
      <br><i>Note that to be eligible for late turn-in with credit, you MUST have attended
          your entire lab period.</i></li>
 </ul>

<hr>
<blockquote>
<h3>Optional Extra Challenge</h3>
<ul>
<li>If you did not close IDLE yet, good. If you did, then open it back up again and
    type a couple of expressions in the Python shell. In both cases, learn how to
    save a "script" of your work in the Python shell. To do this, in
    the Python shell window, use <u>File->Save As</u> to save the transcript
    to lab01.transcript.txt in the original pilot's lab01 directory. During a later
    IDLE session, you can use <u>File->Open</u> to reopen the file as "text" - it is a record
    of your former IDLE session, but not an active session, so results of variable
    assignments and so on will not still exist.</li>
<li>You should also know that it is not necessary to use IDLE to run Python. Your completed
   lab01.py file can be executed directly by Python. If you navigate into your
   lab01 directory (cd ~/cs8/lab01), you should be located in the directory containing
   lab01.py. Then execute the following command:</p>
   <pre>-bash-4.2$ <b>python3 lab01.py</b></pre>
   This should act as if you had attempted <u>Run->RunModule</u> in IDLE.  This is how
   the TAs will grade your programs, so it is useful to test your code one last time
   this way before turning in assignments.</li>
<li>Alternatively, you can just run the Python interpreter directly - without starting
    IDLE and without feeding in a Python program. Try it now - start python, type in some
    expressions and watch the results being displayed. Type exit() to quit. For example:
    <pre>-bash-4.2$ <b>python3</b>
Python 3.3.2 (default, Dec  4 2014, 12:49:00) 
[GCC 4.8.3 20140911 (Red Hat 4.8.3-7)] on linux
Type "help", "copyright", "credits" or "license" for more information.
>>> <b>5 * 4</b>
20
>>> <b>exit()</b>
-bash-4.2$</pre></li>
<li>You learned about using (and even writing simple functions) in text and lectures - and
    you will have do those things in later labs. So if you have time today, why not try
    it out now? Open IDLE, or a Python shell directly - you know how to do both now - and
    try out one or more of the built-in functions like max and min:
    <pre>>>> <b>max(5,7)</b>
7
>>> <b>min(22, -45, 17)</b>
-45</pre>
    To use some functions, it is necessary to import a module, and then to use the module's
    name as part of the function call. For example, the math module has a square root function
    (sqrt), and here is how you would use it:
    <pre>>>> <b>import math</b>
>>> <b>math.sqrt(17)</b>
4.123105625617661
>>> <b>math.sqrt(144)</b>
12.0</pre>
    Type <code>help(math)</code> to learn about more functions from this module, and try some
    of the other functions for the rest of your lab time.</li>
<li>Really? Still have some time after trying out all the math functions you care about?
    Then import turtle, make a turtle like the text and lectures showed you -
    myTurtle=turtle.Turtle() - and make a line drawing of your choice.
    Remember: help(myTurtle) will tell you what you can ask such an object to do. Next week's lab
    will be all about using turtle, so this is just a preview.</li>
</ul>
</blockquote>
 <hr>
 <p>Copyright 2009, Phillip T. Conrad, CS Dept, UC Santa Barbara. Permission to copy
  for non-commercial, non-profit, educational purposes granted, provided appropriate
  credit is given;  all other rights reserved. Adapted by Ziad Matni and Mike Castano for this quarter.</p>
