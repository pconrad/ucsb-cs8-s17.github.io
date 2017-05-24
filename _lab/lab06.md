---
layout: lab
num: lab06
ready: true
desc: "Lab06 - Lists and Dictionaries"
assigned: 2017-05-23 08:00:00.00-7
due: 2017-05-26 23:59:59.00-7
---

<div markdown='1'>

<h1>Lab06: File I/O</h1>
<hr>
<h2>Goals for this lab</h2>

By the time you have completed this lab, you should be able to:
<ol>
<li>Read in data from a file</li>
Match a target string in lines of a file</li>
Know better the difference between printing and returning a function value</li>
</ol>

<h2>Step by Step Instructions</h2>
**Step 0:** Get together with your assigned lab partner.
Select whichever partner was pilot first last time to be navigator first this time. This lab's pilot should log in and create a lab06 directory under your cs8 folder. You will work in this account for the rest of the lab. If your partner is more than 5 minutes late, ask the TA to pair you with someone else for this week.

<b>Log in, and create a lab06 directory</b>.
Decide which one of you will be the first pilot for this lab, and then log in to the pilot's account and create a directory called lab06 inside his/her cs8 folder. You will work in this account for the rest of the lab, but remember to switch often between pilot and navigator roles during the course of the lab.

**Step 1:** Bring up IDLE as usual, and open a new window for function definitions
Start IDLE. Then, select &quot;File-&gt;New Window&quot; and add a comment at the top of this new file like the following (with the proper substitutions of course): 

<pre>
# lab06.py
# Your name(s), date today
# Reading song information from a file
</pre>

Then, save it under the name lab06.py inside your lab06 directory.

**Step 2:** Reading in a file
One thing you might be wondering - how do we get data that populate lists? We do not usually type everything into the Python shell every time. What we want to do is read the information from a file. There are two steps to reading in a file.

<strong>Step 2a: Copy over the file for reading into your working lab06 directory</strong>
Copy the text file from this URL address over to your lab06 directory (ask your lab TA if you are not sure how to do this)

http://www.cs.ucsb.edu/~zmatni/cs8s17/lab6/songs.txt

<strong>Step 2b: Open the file for reading</strong>

The general way to open a file for reading is:

```py
myFile = open(filename,'r') # the 'r' stands for 'read'
```

For this lab, at the bottom of your file, type the line:

```py
myFile = open("./songs.txt","r")   #Assumes the text file is in the same directory as your lab06.py program
```

This will tell Python to open the file of songs information for reading.

<strong>Step 2c: Read in the file, one line at a time</strong>

Python has a special way of reading in a file. Remember how for strings and lists we could write a for loop that iterated once for each character in the string or item in the list? Well, we can write a for loop that iterates once for each line in the file. Add the following after the "open" statement that you already wrote:

```py
for line in myFile:
        print(line)
```
The object named line is a string. Run the module and see what happens. It should print out the contents of the file. Since each line in the file includes a newline character ('\n') at the end, and because the print function also always prints a newline, the output is double-spaced.

Now remove those statements from lab06.py file (or insert '#' in front of each one), so they will not execute every future time you run the module.

**Step 3:** Writing a function to read a file and return a list

Write a function that takes a filename and a target string as input parameters and returns a list of the lines in the file that contain the target string. The function uses the filename to open the file, loops through the lines of the file and saves each line that contains the target string as one element of the list. No printing should be done inside the function - it should just return the list of lines that contain the target string. The function must have the following signature:

```py
def getFileMatches(filename, target):
```

It would be used as follows:

```
>>> filename = "./songs.txt"
>>> loveLines = getFileMatches(filename, "Love")
>>> loveLines
['"When A Man Loves A Woman" - Percy Sledge\n', '"Whole Lotta Love" - Led Zeppel
in\n', '"Sunshine Of Your Love" - Cream\n', '"Bye Bye Love" - The Everly Brother
s\n', '"Somebody To Love" - Jefferson Airplane\n', '"Where Did Our Love Go" - Su
premes\n', '"She Loves You" - Beatles\n', '"(Love Is Like A) Heat Wave" - Martha
 & The Vandellas\n', '"Why Do Fools Fall In Love?" - Frankie Lymon & Teenagers\n
 ', '"I\'d Love To Change The World" - Ten Years After\n', '"Who Do You Love?" -
 Bo Diddley\n', '"Stop! In The Name Of Love" - The Supremes\n', '"What\'s Love Go
 t To Do With It?" - Tina Turner\n', '"Love Hurts" - Nazarath\n', '"Pride (In The
  name Of Love)" - U2\n', '"I Love Rock \'n\' Roll" - Joan Jett & The Blackhearts
  \n', '"Love The One You\'re With" - Stephen Stills\n']
  ```

  Hints: This is a problem in which you build the solution gradually. What type of problem is this? You are returning a list - think carefully about what the list should start out as (initialization). How do you think you express that a variable is set to a list with no items in it? Then, how do you find out which lines to add to the list based on whether or not the target string is in the line?

**Step 4:** A function to print lines of a file

<strong>Switch roles between pilot and navigator</strong>

So that you can more neatly demonstrate to the TAs that you have completed your task - and to learn more clearly the difference between a function that returns a result and a function that prints results for the user to see - write a function that takes in a filename and a target string as parameters, calls your *getFileMatches* function, stores the result into a list, and then prints out each element of the list. For example:

>>> filename = "./songs.txt"
>>> printFileMatches(filename, "We")
"We Will Rock You" - Queen

"The Weight" - The Band

"Welcome To The Jungle" - Guns N' Roses

"Werewolves of London" - Warren Zevon

"We're An American Band" - Grand Funk Railroad

"We Gotta Get Out Of This Place" - Animals

Don't worry about printing the extra newline characters that are part of each line. Of course, if that bothers you then you can get rid of the extra lines in more than one way. Let's say a line of the file is stored in a string called line, then any of the following would print just one of the two newline characters:

>>> print(line[:-1])  # prints all except the last character in line
>>> print(line.strip())  # prints line with no leading/trailing white space
>>> print(line, end='')  # replaces the usual '\n' at the end with ''

**Step 5:** Using the split() member function for lists
The data in "songs.txt" are arranged so that each line contains a song title, a separator (" - "), and an artist. The split function can be told to use a different delimiter than space, and in this case it can be told to use " - " as the delimiter to get the two important pieces out of the data. For example, here is the result for the first line:

```
>>> line.split(" - ")
['"Stairway to Heaven"', 'Led Zeppelin\n']
```

Write and test another function to return two lists (or one list of tuples) for songs and artists, given the name of a file such as songs.txt. Try to clean up the results too, by removing the newline character ('\n') from the end of the artist name, and maybe the quote characters (") around the song title.

**Step 6:** Show off your work and get credit for the lab

<table bgcolor="yellow" border="1" cellpadding="4"><tbody><tr><td>
   Get your TA's attention to inspect your work, and to record your lab completion.
</td></tr></tbody></table>

<blockquote>
**Step 6a.**
Submit your with the turnin program. You MUST have both your name and your partner's name in the file in order to receive credit. Remember that the original pilot needs to do this step, since that is whose account you have been using in Phelps 3525. Use the following command after you cd into your cs8/lab06 directory:

<pre>turnin Lab06@cs8 lab06.py</pre>

After answering the questions, be sure to <em>wait for the message indicating success.</em>
</blockquote>

<hr>
<h2>Evaluation and Grading</h2>
Each student must accomplish the following to earn full credit for this lab:
 <ul>
   <li>lab06.py is saved in original pilot's ~/cs8/lab06/ directory.</li>
 </ul>

<hr>
Prepared for Computer Science 8 by Ziad Matni based on a creation by Mike Costanzo and Diana Franklin, (c) 2017.

</div>
