---
layout: lab
num: lab04
ready: true
desc: "Lab04 - Strings, and Program Testing"
assigned: 2017-05-03 08:00:00.00-7
due: 2017-05-05 23:59:59.00-7
---

<div markdown='1'>

<h1>Lab04: Strings, and Program Testing</h1>
<hr>
<h2>Goals for this lab</h2>

By the time you have completed this lab, you should be able to:
<ol>
<li>Use Python strings and string variables </li>
<li>Create test-cases for your programs </li>
</ol>

<h2>Step by Step Instructions</h2>
**Step 0:** Get together with your assigned lab partner.
Select whichever partner was pilot first last time to be navigator first this time. This lab's pilot should log in and create a lab04 directory under your cs8 folder. You will work in this account for the rest of the lab. If your partner is more than 5 minutes late, ask the TA to pair you with someone else for this week.

**Step 0:** Log in, and create a lab04 directory
Decide which one of you will be the first pilot for this lab, and then log in to the pilot's account and create a directory called lab04 inside his/her cs8 folder. You will work in this account for the rest of the lab, but remember to switch often between pilot and navigator roles during the course of the lab.

**Step 1:** Bring up IDLE as usual, and open a new window for function definitions
Start IDLE. Then, select &quot;File-&gt;New Window&quot; and add a comment at the top of this new file like the following (with the proper substitutions of course): 

<pre>
# lab04.py
# Your name(s), today's date
# a cipher function and test cases
</pre>

Then, save it under the name lab04.py inside your lab04 directory.

**Step 2:** Design rot13 cipher
You have been hired as a programmer! Your mission is to write a program that encrypts a string of text. See Exercise 3.26 on page 108 of the text (rot is short for rotate):

```
Encryption often involves the Caesar cipher - named after Julius Caesar, who used the system to encrypt military messages. 
Many early Internet users also adopted this cipher. Called rot13, the cipher encrypts a message by rotating the 
plaintext character by 13 positions in the alphabet. For example, "a" becomes "n" and likewise "n" becomes "a". 
The nice thing about rot13 is that the same function can be used to encrypt and decrypt a message.
```

Write function rot13 - it takes a message as a parameter, and it returns an encrypted string in which all the characters in the message are rotated by 13 places. You may assume that all characters in the message are lower case letters (no upper case letters, spaces, digits or anything else). Here is a skeleton of the function. We have initialized an important variable, and given in-line comments to help you out.

```
def rot13(message):
    result = ""   # starts empty; add one character at a time below

	# loop through each character
    # shift it by 13 places (may wrap around to front of alphabet)
    # add it to the result string
```
Of course you should return the result at the end too.

Hints: Remember the chr() and ord() functions from lecture. Find a mathematical formula that will take the number of one character and transform it to the number of the desired character. You may find the '%' (modulus) operator helpful in your formula.

**Step 3:** Test rot13 cipher

Switch roles between pilot and navigator. The job of the new pilot is to create test strings to test the function. What characters should be in each string in order to fully test the encryption function? How can you test that the function will encrypt a string, and then accurately decrypt the resulting string?

Write the test code below the function definition - not as an indented part of the function itself. This way by running the module, your test cases will execute automatically. Make sure you print to the screen both the original string and the encrypted string.

Be ready to demonstrate your function and test cases to a TA.

**Step 4:** Design and test a more flexible rot cipher
Write and test an encryption function that shifts by a variable number of positions rather than always 13. Just name it rot, but have it take two arguments:

```
def rot(n, string):
```

The first parameter, n is the number of positions by which to shift. So if if n is 13, then rot produces the same result as rot13. The results are different for other values of n though. Here are two example runs from our solution:

```
>>> rot(1,'apple')
'bqqmf'
>>> rot(2,'apple')
'crrng'
```

By the way, with our solution, a string that was previously encrypted by shifting n positions can be decrypted by passing -n to rot:

```
>>> rot(-2,'crrng')
'apple'
```

**Step 5:** Show off your work and get credit for the lab

<table bgcolor="yellow" border="1" cellpadding="4"><tbody><tr><td>
   Get your TA's attention to inspect your work, and to record your lab completion.
</td></tr></tbody></table>

<blockquote>
**Step 5a.**
In the unlikely event that you must complete this assignment at CSIL, then submit it with the turnin program. You MUST have both your name and your partner's name in the file in order to receive credit. Remember that the original pilot needs to do this step, since that is whose account you have been using in Phelps 3525. Use the following command after you cd into your cs8/lab04 directory:

<pre>turnin Lab04@cs8 lab04.py</pre>

After answering the questions, be sure to <em>wait for the message indicating success.</em>
</blockquote>

<hr>
<h2>Evaluation and Grading</h2>
Each student must accomplish the following to earn full credit for this lab:
 <ul>
   <li>lab04.py is saved in original pilot's ~/cs8/lab04/ directory.</li>
   <li>lab04.py is saved, and the encrypt function as well as the test cases are working properly (the module should run without errors, and produce test output in the Python shell). </li>
 </ul>

<hr>
Prepared for Computer Science 8 by Ziad Matni as inspired from lab ideas from Diana Franklin and Michael Costanzo.

</div>
