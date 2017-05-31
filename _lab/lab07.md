---
layout: lab
num: lab07
ready: false
desc: "Lab07 - Loops and Images"
assigned: 2017-05-31 08:00:00.00-7
due: 2017-06-02 23:59:59.00-7
---

<div markdown='1'>

<h1>Lab07: While Loops and Image Processing</h1>

<hr>
<h2>Goals for this lab</h2>

By the time you have completed this lab, you should be able to:
<ol>
<li>Use a while loop to get data from a user</li>
<li>Use cImage module to display an image</li>
</ol>

<h2>Step by Step Instructions</h2>
**Step 0:** Get together with your assigned lab partner.
Select whichever partner was pilot first last time to be navigator first this time. This lab's pilot should log in and create a lab07 directory under your cs8 folder. You will work in this account for the rest of the lab. If your partner is more than 5 minutes late, ask the TA to pair you with someone else for this week.

<b>Log in, and create a lab07 directory</b>.
Decide which one of you will be the first pilot for this lab, and then log in to the pilot's account and create a directory called lab07 inside his/her cs8 folder. You will work in this account for the rest of the lab, but remember to switch often between pilot and navigator roles during the course of the lab.

**Step 1:** Bring up IDLE as usual, and open a new window for function definitions
Start IDLE. Then, select &quot;File-&gt;New Window&quot; and add a comment at the top of this new file like the following (with the proper substitutions of course): 

<pre>
# lab07.py
# Your name(s), date today
# Function to get a list of strings from the user
</pre>

Then, save it under the name lab07.py inside your lab07 directory.

**Step 2:** Practice getting text from a user and applying a while loop
Working in the Python shell window, type the following statement, then enter some text in response to the question, and finally display the text:

```
>>> text = input("enter some text: ")
enter some text: here I am entering text
>>> text
'here I am entering text'
```

Next fill a list with text the user enters, until the user types "quit" (without the quotes). This will be accomplished using a while loop, but you must get the first text item before the loop begins (this is the initialization step):

```
>>>item = input("enter item: ")
enter item: Hi
```

Now create a new empty list and start a while loop that continues until the item equals "quit". Inside the body of the loop, append the current item to the list and get the next item:

```
>>> textList = [ ]
>>> while (item != "quit"):
    textList.append(item)
        item = input("enter item: ")
```

After you enter this code followed by a blank line, the program will repeatedly get text items from the user (you in this case). After typing quit, then display the list:

```
enter item: this is
enter item: lots and lots
enter item: of fun
enter item: quit
>>> textList
['Hi', 'this is', 'lots and lots', 'of fun']
```

**Step 3:** Function to get a list of text items from user

Write a function (in the lab07.py file) named <strong>getStrings</strong> to do essentially what you practiced above and then return (not print) the list. Instead of instructing the user to "enter item" for each item though, please just ask once and also let the user know to enter "quit" when done. Then just use ": " to prompt the user to enter each item. Here is an example run followed by a display of the resulting list:

```
>>> itemList = getStrings()
Enter items; enter "quit" to quit
: apple
: pear
: orange
: quit
>>> itemList
['apple', 'pear', 'orange']
```

Test your function from the Python shell window and verify it works properly. Notice that "quit" is not one of the items stored in the list.

Please do not spend so much time on this step that you won't have time for Step 4 during lab - save 15 minutes to be safe. You can come back to this step again later if necessary.

**Step 4:** Practice displaying an image with the `cImage` module

<strong>Switch roles between pilot and navigator.</strong>

First you must gain access to the text's cImage module. There is a copy in the directory named lib in the cs8 class account, so that directory must be added to the system's path list in order to import it later:

```
>>> import sys
>>> sys.path.append('/cs/class/cs8/lib')
```

Find out right now if it worked:

```
>>> from cImage import *
```

Ask for help if you get an error message.

There is a small image of the UCSB campus in the same directory as the cImage module. Type the following to get that image and assign the name image to it:

```
>>> image = FileImage('/cs/class/cs8c/lib/campus.gif')
```

Still no error messages? Great! Now find out the size of this image (in pixels), and store its dimensions in variables named width and height:

```
>>> width = image.getWidth()
>>> height = image.getHeight()
```

Go ahead and type width to learn the width, and height to learn the height, but you will use the variables in the next step so no need to memorize the values. Now create a window in which to draw the image - make it exactly the right size by using the width and height variables:

```
>>> window = ImageWin("UCSB", width, height)
```

You should see an empty window on your desktop with the title, UCSB. Finally, tell the image object to draw itself in this window:

```
>>> image.draw(window)
```

Wait for it ...

Leave the image window open for a TA to see. Go back and finish Step 3 if necessary, and be ready to demonstrate your <strong>getStrings<\strong> function to the TA too.

**Step 5:** Show off your work and get credit for the lab

<table bgcolor="yellow" border="1" cellpadding="4"><tbody><tr><td>
   Get your TA's attention to inspect your work, and to record your lab completion.
</td></tr></tbody></table>

<blockquote>
**Step 5a.**
Submit your with the turnin program. You MUST have both your name and your partner's name in the file in order to receive credit. Remember that the original pilot needs to do this step, since that is whose account you have been using in Phelps 3525. Use the following command after you cd into your cs8/lab07 directory:

<pre>turnin Lab07@cs8 lab07.py</pre>

After answering the questions, be sure to <em>wait for the message indicating success.</em>
</blockquote>

<hr>
<h2>Evaluation and Grading</h2>
Each student must accomplish the following to earn full credit for this lab:
 <ul>
   <li>lab07.py is saved in original pilot's ~/cs8/lab07/ directory.</li>
 </ul>

<hr>
Prepared for Computer Science 8 by Ziad Matni based on a creation by Mike Costanzo and Diana Franklin, (c) 2017.

</div>
