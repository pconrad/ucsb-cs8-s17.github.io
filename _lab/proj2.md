---
layout: lab
num: project2
ready: true
desc: "Reading file/URL inputs and processing/formatting the results"
assigned: 2017-05-19 08:00:00.00-7
due: 2017-06-06 23:59:59.00-7
---
<div markdown="1">

<h1> NOT READY! DO NOT USE YET!</h1>

<h1>CS 8, Spring 2017: Programming Project 2</h1>
<h2>Due: Friday, 6/2 11:59pm</h2>

It is optional, but highly recommended, to work with a partner on this project. 

<h2>CountChars.py</h2>
(100 points: reading from file or URL, formatting strings, data structures)

Begin a new file named <strong>CountChars.py</strong> by typing a comment at the top with your name (and the name of your lab partner if you work together), and the current date.

You will notice the instructions are a bit shorter this time. You are given a problem to solve, <em>but you must figure out how to solve it yourself</em>. Keep in mind what you have learned about top-down programming by stepwise refinement: break the problem into meaningful parts; then solve each part separately. And have fun!

The problem is to write a Python3 program that reads a text file or web page named by the user, and prints a neat table showing the counts of all of the different characters it reads. You must also meet the following explicit specifications:

Since we insist that your output will exactly match the results of our solution (see the 3 examples below), copy the following string and dictionary constants and paste them to the beginning of countchars.py (after your header comment of course):

```py
# strings that must be used for output:
prompt = "Enter filename: "
titles = "char       count\n----       -----"
itemfmt = "{0:5s}{1:10d}"
totalfmt = "total{0:10d}"
whiteSpace = {' ':'space', '\t':'tab', '\n':'nline', '\r':'crtn'}
```

Make it so that when you run the module in IDLE, it should immediately instruct the user to enter the filename, and then it should print the table of counts in the Python shell window. Alternatively, a user can run the program directly from the command prompt without ever starting Python or IDLE, by typing the following:

```
-bash-4.2$ python3 CountChars.py
```

Execution must proceed as follows:

<ol markdown="1">
<li>Use the built-in function input to get the filename from the user. Pass the string named prompt to this function.</li>

<li>If the filename does not begin with "http" then assume it is a local file, and open it for reading with the built-in open function. Otherwise import and use the urllib.request.urlopen function to open the web page for reading. The program has to be able to do this automatically.</li>

<li>Read all of the text in the file or web page, and count each different character in it. Ignore the case of characters (e.g., count both 'A' and 'a' as 'a').</li>

<li>Print the string named <strong>titles</strong>. Then print the table of characters and their counts in ASCII order, and print the total character count at the bottom.</li>

<li>Use the string named <strong>itemfmt</strong> to print each interior row of the table in the proper format. For example, if c is a character, and ccount is its count, then print that row of the table as follows:</li>

<div markdown="1">
```py
print( itemfmt.format(c, ccount) )
```
</div>

<li>If the character being printed is one of the white space characters in the dictionary named <strong>whitespace</strong>, then print its description instead of the character itself. For example:</li>

<div markdown="1">
```py
print( itemfmt.format(whiteSpace[c], ccount) )
```
</div>

<li>Use the string named <strong>totalfmt</strong> to properly print the total character count. If this count is named <strong>total</strong>, for example:</li>

<div markdown="1">
```py
print( totalfmt.format(total) )
```
</div>

<li>Fully test your program. Here are sample input files and web pages, and the associated results from our solution. Make sure that your results <em><strong>exactly match these results</strong></em>. Also realize that the graders will probably test other inputs too.</li>

<div markdown="1">

|File/Page|Program Run|
|---------|-----------|
|<a href="http://www.cs.ucsb.edu/~zmatni/cs8s17/projects/proj2/short.txt">short.txt</a>|<a href="http://www.cs.ucsb.edu/~zmatni/cs8s17/projects/proj2/shortsample.txt">short.txt run</a>|
|<a href="http://www.cs.ucsb.edu/~zmatni/cs8s17/projects/proj2/longer.txt">longer.txt</a>|<a href="http://www.cs.ucsb.edu/~zmatni/cs8s17/projects/proj2/longersample.txt">longer.txt run</a>|
|<a href="http://www.cs.ucsb.edu/~zmatni/cs8s17">http://cs.ucsb.edu/~zmatni/cs8s17</a>|<a href="http://www.cs.ucsb.edu/~zmatni/cs8s17/projects/proj2/webpagesample.txt">CS8 Home Page run</a>|
</div>

<hr>
Go to CSIL (in person unless you can manage this step remotely without any assistance from us). Open a terminal window, <code>cd</code> to the
<em>same directory as your source code files</em>, then type the following (careful - turning in to uppercase P, Proj2, at class account cs8):
<pre>turnin Proj2@cs8 CountChars.py</pre> 

If you are working with a partner, be sure that <em>both partners names</em> are in the comments at the top of all source files.

If you run into problems, be sure to ask questions on Piazza or visit your TA's or your instructor's office hours.

<hr>
Created by Ziad Matni, (c) 2107, partly based on prior work by M. Costanzo and others.
