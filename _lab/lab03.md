---
layout: lab
num: lab03
ready: false
desc: "Lab03 - Accumulator Functions and User Input"
assigned: 2017-04-26 08:00:00.00-7
due: 2017-04-28 23:59:59.00-7
---

<div markdown='1'>

<h1>Lab03: Factorial Function & Coin Counter</h1>
<hr>
<h2>Goals for this lab</h2>

By the time you have completed this lab, you should be able to:
<ol>
<li>Write functions that use what the textbook calls the "Accumulator Pattern"</li>
<li>Write functions that get user inputs from standard input devices (i.e. keyboard).</li>
</ol>


<h2>Step by Step Instructions</h2>
**Step 0:** Get together with your assigned lab partner.

**Step 1:** Log in, and create a lab03 directory
Decide which one of you will be the first pilot for this lab, and then log in to the pilot's account and create a directory called lab03 inside his/her cs8 folder. You will work in this account for the rest of the lab, but remember to switch often between pilot and navigator roles during the course of the lab.

**Step 2:** Bring up IDLE as usual, and open a new window for function definitions
Start IDLE. Then, select &quot;File-&gt;New Window&quot; and add a comment at the top of this new file like the following (with the proper substitutions of course): 

<pre>
# lab03.py
# Your name(s), today's date
# a factorial function and a coin counter function
</pre>

Then, save it under the name lab03.py inside your lab03 directory.

**Step 3:** Practice writing a function to accumulate products

(Exercise 2.12 from page 56 of the text). Together we will write a function called factorial that computes the product of the first N numbers, where N is a parameter. For example, factorial(4) is calculated as 1 * 2 * 3 * 4, so the function should return the value 24. We will assume N is greater than 0.

Be sure to understand the purpose and meaning of each of the following instructions before you execute them.

<ol type="a">

<li>Skip a blank line (in your lab03.py file), and then type a brief comment for a factorial function such as the following:
  <pre>
  # factorial - returns n factorial 
  # assumes n is greater than or equal to 0
  </pre>
</li>

<li>On the very next line, type the function header as follows:
  <pre>def factorial(n):</pre>
</li>

<li>We need an "accumulator" variable for the result. Since the accumulation will be multiplicative (instead of additive), this variable should be initialized to 1 (and the statement must be indented as it is inside the function):
  <pre>
  result = 1
  </pre>
</li>

<li>Now it is time to loop through the values that must be multiplied, and we will use the Python range function for the purpose. First let's <em>think</em> about the sequence we need to multiply: 1*2*...*n. We can skip the 1 and still get the same result, but we can't skip the n. So that means we can start the range at 2, but the stop value must be n+1 to include n as the last value. Inside the loop we must do the multiplications and <em>accumulate</em> the product in our result variable. Here is the whole thing (since we already initialized result to 1 above; and notice the body of the loop is indented one more time):
  <pre>    
  for i in range(2, n+1):
        result = result * i
</pre>
</li>

<li>Just one last thing to do is return the result, and then type a blank line to indicate the function is complete:
  <pre>    
  return result
  </pre>
</li>
</ol>

Save and run the module. Then test the function a few times (in the Python shell window) by comparing its results to ones that you calculate manually.  Here is one example run of our solution:
<pre>
>>> <b>factorial(5)</b>
120
</pre>

**Step 4:** Couting Coins

Write a program that allows the user to enter a number of quarters, dimes, and nickels and then outputs the monetary value of the coins in cents. For example, if the user enters 2 for the number of quarters, 3 for the number of dimes, and 1 for the number of nickels, then the program should output that the coins are worth 85 cents.

The program should ask the user by printing out a question (output) and the wait for the user to answer it (input). User input is followed by pressing the RETURN key.

We have learned how to handle outputs to standard devices, i.e. using the <b>print( )</b> function. But how do we handle inputs? In Python, use the built-in function <b>input( )</b>, like this example, which you can try out in the Python interpreter:
<pre>
>>> <b>name = input("What is your name? ")</b>
What is your name? <b>Jimbo</b>
>>> <b>name</b>
'Jimbo'
</pre>

The default for <b>input( )</b> is that the variable is a string, like <b>name</b> = 'Jimbo' in the previous example. So you can use the variable as you would any string, for example (continuing from the prior example):
<pre>
>>> <b>len(name)</b>
5
>>> <b>name[2]</b>
'm'
</pre>

If the user had entered 33 at the input prompt, then the variable <b>name</b> would now hold '33' as a string (not as a number!) If you want to ensure that the input is accepted as something else, like an integer, then do as this example shows (note how we would modify the input( ) function):
<pre>
>>> <b>number = int( input("What is your age? ") )</b>
What is your age? <b>21</b>
>>> <b>number</b>
21
>>> <b>number + 10</b>
31
</pre>

Just as you did with the previous function, skip a blank line (in your lab03.py file), and then type a brief comment, followed by the function header (what will you call this function?)

This function should print a string of text to the terminal before getting each piece of input from the user. A session should look like the following example with possibly different numbers for inputs and the output (so the following is just ONE example of how the function might run):
<pre>
Enter number of quarters: <b>4</b>
Enter number of dimes: <b>12</b>
Enter number of nickels: <b>3</b>
The total is: 235 cents.
</pre>

**Step 5:** Show off your work and get credit for the lab

<table bgcolor="yellow" border="1" cellpadding="4"><tbody><tr><td>
   Get your TA's attention to inspect your work, and to record your lab completion.
</td></tr></tbody></table>

<blockquote>
**Step 5a.**
Your final submission, lab03.py, should now have 2 functions defined therein: one for the factorial function and the other for the coin counter function.

In the unlikely event that you must complete this assignment at CSIL, then submit it with the turnin program. You MUST have both your name and your partner's name in the file in order to receive credit. Remember that the original pilot needs to do this step, since that is whose account you have been using in Phelps 3525. Use the following command after you cd into your cs8/lab03 directory:

<pre>turnin Lab03@cs8 lab03.py</pre>

After answering the questions, be sure to <em>wait for the message indicating success.</em>
</blockquote>

<hr>
<h2>Evaluation and Grading</h2>
Each student must accomplish the following to earn full credit for this lab:
 <ul>
   <li>Turn in a complete and accurate Hw3.</li>
   <li>lab03.py is saved in original pilot's ~/cs8/lab03/ directory.</li>
   <li>lab03.py contains a working factorial function.</li>
   <li>lab03.py contains a working coin counter function.</li>
 </ul>

<hr>
Prepared for Computer Science 8 by Ziad Matni, partly based on an idea by Diana Franklin and Michael Costanzo.

</div>
