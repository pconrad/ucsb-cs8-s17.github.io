---
layout: lab
num: lab05
ready: false
desc: "Lab05 - Lists and Dictionaries"
assigned: 2017-05-10 08:00:00.00-7
due: 2017-05-19 23:59:59.00-7
---

<div markdown='1'>

<h1>Lab05: Using Lists and Dictionaries</h1>
<hr>
<h2>Goals for this lab</h2>

By the time you have completed this lab, you should be able to:
<ol>
<li>Use Python lists and dictionaries</li>
</ol>

<h2>Step by Step Instructions</h2>
**Step 0:** Get together with your assigned lab partner.
Select whichever partner was pilot first last time to be navigator first this time. This lab's pilot should log in and create a lab05 directory under your cs8 folder. You will work in this account for the rest of the lab. If your partner is more than 5 minutes late, ask the TA to pair you with someone else for this week.

**Step 0:** Log in, and create a lab05 directory
Decide which one of you will be the first pilot for this lab, and then log in to the pilot's account and create a directory called lab05 inside his/her cs8 folder. You will work in this account for the rest of the lab, but remember to switch often between pilot and navigator roles during the course of the lab.

**Step 1:** Bring up IDLE as usual, and open a new window for function definitions
Start IDLE. Then, select &quot;File-&gt;New Window&quot; and add a comment at the top of this new file like the following (with the proper substitutions of course): 

<pre>
# lab05.py
# Your name(s), date today
# Some list and dictionary functions
</pre>

Then, save it under the name lab05.py inside your lab05 directory.

**Step 2:** Design a function to print list elements
Write a function named printSortedList to print the sorted elements of a list with labels showing the sorted order of each element. The sorting should be done in ascending order. The function header should like this:

```
def printSortedList(aList):
```

And here is an example run:

```
>>> myList = [92.5, 127.1, 9, 104.2, 78.4]
>>> printSortedList(myList)
1 9
2 78.4
3 92.5
4 104.2
5 127.1
```

Test your function from the Python shell window on various types of lists with varying lengths.

**Step 3:** Test out a program from the textbook to visualize a frequency distribution

Switch roles between pilot and navigator. Prepare for this part by reading <b>section 4.6.3</b> in your textbook and apply the function described in <b>listing 4.10</b> on a list of:

```
ListA = [1, 3, 4, 1, 1, 5, 9, 8, 5, 6, 4, 4, 5, 3]
```

Call your function <b>freqDistVisual()</b>.

What do you see when you apply the function on the above list? Does it conform to the example diagram shown in the textbook (on page xxx)? Take a screenshot of the resulting drawing, save it as "Lab5.Fig1.jpg" (or .png or .gif) and include it with your lab submission.

Be ready to demonstrate your function and test cases to a TA.

**Step 4:** Modify the program from Step 3

You now have to modify the frequency chart function to draw *wider* bars instead of lines. Make the width of the bars appropriately wide (you might have to experiment a bit with this). Call this function <b>freqDistVisual2()</b>.

Take a screenshot of the resulting drawing, save it as "Lab5.Fig2.jpg" (or .png or .gif) and include it with your lab submission.

Be ready to demonstrate your function and test cases to a TA.

**Step 5:** Show off your work and get credit for the lab

<table bgcolor="yellow" border="1" cellpadding="4"><tbody><tr><td>
   Get your TA's attention to inspect your work, and to record your lab completion.
</td></tr></tbody></table>

<blockquote>
**Step 5a.**
In the unlikely event that you must complete this assignment at CSIL, then submit it with the turnin program. You MUST have both your name and your partner's name in the file in order to receive credit. Remember that the original pilot needs to do this step, since that is whose account you have been using in Phelps 3525. Use the following command after you cd into your cs8/lab05 directory:

<pre>turnin Lab05@cs8 lab05.py</pre>

After answering the questions, be sure to <em>wait for the message indicating success.</em>
</blockquote>

<hr>
<h2>Evaluation and Grading</h2>
Each student must accomplish the following to earn full credit for this lab:
 <ul>
   <li>lab05.py and the 2 screenshot pictures are saved in original pilot's ~/cs8/lab05/ directory.</li>
   <li>The functions printSortedList(), freqDistVisual(), freqDistVisual2() are working properly (the module should run without errors, and produce test output in the Python shell). </li>
 </ul>

<hr>
Prepared for Computer Science 8 by Ziad Matni, (c) 2017.

</div>
