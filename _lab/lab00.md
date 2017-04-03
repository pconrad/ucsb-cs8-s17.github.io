---
layout: lab
num: lab00
ready: true
desc: "Lab00 - A gentle introduction"
assigned: 2017-04-04 08:00:00.00-7
due: 2017-04-05 19:00:00.00-7
---
<h2>Introduction</h2>

<p>Your first lab for this week is an introduction to programming on CSIL and in the Computer Science lab. You will write your first Python program that will print a specific text out on your computer display.</p>

 <h2>Goals for this lab</h2>
 <p>By the time you have completed this lab, you should be able to </p>
 <ul>
   <li>use the computers in Phelps 3525 (and other labs like CSIL) to do basic things</li>
   <li>perform basic management of directories and files</li>
   <li>know how to submit assignments using the &quot;turnin&quot; program.</li>
</ul>
 <p>Additionally, most of you will have a lab partner to share lab and
 some other duties during the rest of the quarter.</p>
 <p>This assignment is designed to make sure you are comfortable working in the 
computing environment and know how to submit your work. It is mostly about
mechanics, not concepts. As a result, this assignment is not particularly intellectually
challenging. We hope that will not be the case in future labs!</p>

 <h2>Step by Step Instructions</h2>

 <h3>Step 0: Select a lab partner</h3>
 <p>Refer to your responses to question 1 of Hw0: "What of the following things have you done before?"</p>
 <ul>
    <li>If you circled just "a" and/or "b" then we consider you a relative beginner, and we think that you
    should select a partner who is also a beginner like yourself.</li>
    <li>If you circled "c" and/or "d" then we think you should select a partner who is a bit more
    experienced, like we consider you to be.</li>
    <li>No more than one student each lab is allowed to work without a partner, and only then if
    there is not an even number of students in the lab. The TAs will ensure that any such lone
    worker has circled "c" and/or "d" in response to that experience question.</li>
 </ul>
 <p>Does your experience match the person with whom you are currently paired? Do you both want to
    work with each other? If the answer is no to either of those questions, then look around to find
    a different partner now.</p>
 <p>We expect a few minutes of (hopefully not chaotic) mingling while you match up, but please try
    to do it quickly. You can refer to responses to question 2, "What type of computer/system(s) do
    you have?" if that matters to you. Research also shows that lab partners are best matched by
    gender, but we leave that decision to you too.</p>
 <p>We expect you to keep the partner you select today to work with in future labs. Please inform us if
    you make any changes later.</p>
 <p>Before proceeding to Step 1, fill in your partner's name and CoE username (if available) in
    response to question 4 of Hw0.'</p>

 <h3>Step 1: Verify your College of Engineering Account(s)
  <span class="smallerFont">[SHOULD BE DONE ALREADY!]</span></h3>
 <p>For Hw0 you were instructed to create (or confirm the existence of) a &quot;College of
 Engineering&quot; computer account. One of you must already be signed on (or you would not be
 reading this page right now), but we need to make sure that both of you can do that. So log out
 and let your partner log in now.</p>
 <p>If either of you have arrived at your lab session without ever logging:</p>
 <ul>
   <li>Stay logged into whichever account you are using now. If none, then a TA can log onto a
       different computer, and provide a web browser for you to use to fill out
       the form necessary to create the account. Go to the following link to do so:
       <br><a href="https://accounts.engr.ucsb.edu/create/">https://accounts.engr.ucsb.edu/create</a>
   </li>
   <li>Once you create the account, it may take several minutes before the account is active.</li>
   <li>After waiting 5-10 minutes, try logging in.</li>
  </ul>
  <p>Problems? Scroll to the <a href="#problem">bottom</a> of this web page to find out what to do.</p>

<h4>Notes:</h4>
 <ul>
   <li>Phelps 3525 is only available during your weekly scheduled discussion section - it
   is not open for your use at other times.</li>
   <li>At other times during the week, you can work in CSIL, the &quot;Computer Science
   Instructional Lab&quot;.
   <br><strong>Finding CSIL:</strong> CSIL is located in Harold Frank Hall (HFH).
    You enter from an outside door. To locate CSIL, find the &quot;main front entrance&quot;
    to Harold Frank Hall, on the side of the building that faces the ocean. Stand <em>outside</em>
    the double glass doors, with your <em>back</em> to the building, <em>facing the ocean</em>.
    The entrance to CSIL is now on your <em>left</em>.</li>
 </ul>
 <p>If you are making up this lab assignment outside your regularly scheduled lab time (because
    you added the course late for example), then you should go to CSIL to do it.
 </p>

<table bgcolor="lightcyan" border="1" cellpadding="4"><tbody><tr><td>
   <strong>Steps 2 through 8 below must be done once for each lab partner.</strong>
   <br>First complete these steps for whichever partner is currently logged on. After Step 8,
   you must go back and redo the steps using the other partner's account.
</td></tr></tbody></table>

<h3>Step 2: Bring up a terminal window</h3>
 <p>On the Linux systems, there a lot of things we can do with pointing and clicking
 with the mouse, just like on Windows or Mac. But there are also many things we can
 only do with the command line, or can do more easily with the command line.</p>
 <p>So, one of the first steps will often be to bring up a &quot;Terminal Window&quot;,
 which is the Linux &quot;command line&quot;.</p>
 <p>Here's how:</p>
 <ul>
   <li>Find the Applications Menu at the top left of the screen.</li>
   <li>Select System Tools, then Terminal Window</li>
   <li>A Terminal Window should pop up.</li>
  </ul>

<h3>Step 3: Make sure your username/password work on both systems</h3>
 <p>If you are working in Phelps 3525, before we go any further, we need to make sure
  that your username/password also work on the CSIL computers.</p>
 <p>If you are working in CSIL (e.g. because you missed the first week's lab and are making
 it up by working in CSIL), we need to make sure your username/password also work on the
  Phelps 3525 computers.</p>
 <p>This is just a &quot;check&quot; to see if there are any problems with your account.</p>
 <h4>What we are going to do</h4>
 <p>We will try your username/password over the internet using a program called ssh, which
 stands for secure shell.</p>
 <ul>
   <li>If we are successful, we'll just immediately log out, and move on to Step 6. </li>
   <li>If it doesn't work after 15 minutes, we'll need you to send an email to support.</li>
  </ul>
 <h4>Here's how to do it (if you are in Phelps 3525)</h4>
 <p>In the Terminal Window that you brought up in the previous step, enter the following
 command:</p>
 <pre>ssh csil.cs.ucsb.edu</pre>
 <p>When you type this at the Unix command line, you may see something like this:</p>
 <pre>-bash-4.2$ <strong>ssh csil.cs.ucsb.edu</strong>
The authenticity of host 'csil.cs.ucsb.edu (128.111.43.14)' can't be established.
RSA key fingerprint is 90:ab:6a:31:0b:81:62:25:9b:11:50:05:18:d3:1a:b5.
Are you sure you want to continue connecting (yes/no)?</pre>
 <p>Answer the question by typing <strong>yes</strong>, and pressing &quot;enter&quot;
 (or &quot;return&quot;)</p>
 <p>Then, you'll be prompted for your password.</p>
 <p><strong>Again, don't worry if nothing appears on the screen while you are typing
 your password.</strong></p>
 <p>If it worked, you'll see something like this:</p>
 <pre>jimbo@csil.cs.ucsb.edu's password: 
Last login: Tue Dec 30 12:27:04 2014 from linux32.engr.ucsb.edu

Welcome to Computer Science's Remote Access server -- csil.cs.ucsb.edu

You may run your graphically intensive programs on specific workstations in CSIL.
-bash-4.2$</pre>
 <p>Now we know that you can connect to CSIL.
<br><table border="1" cellpadding="4" bgcolor="yellow"><tr><td>
   Get your TA's attention so he/she can verify you are logged into CSIL. And turn
   in Hw0 at this time too.
</td></tr></table>
<br>Then exit from the session on CSIL by typing the word <strong>exit</strong>,
 like this:</p>
 <pre>-bash-4.2$ <strong>exit</strong>
logout
Connection to csil.cs.ucsb.edu closed.
-bash-4.2$ </pre>
 <p>If you are ever not sure whether you are logged in to CSIL or not, you can type
 the command <strong>hostname</strong> at the command prompt. If you are logged into
 CSIL, it will look like this:</p>
 <pre>-bash-4.2$ <strong>hostname</strong>
csil.cs.ucsb.edu
-bash-4.2$ </pre>
  <h4>If you are in CSIL instead</h4>
 <p>If you are working in CSIL, we need to make sure your username/password also work
 on the Phelps 3525 computers.<br>
    <br>
  The instructions are exactly the same as those for Phelps 3525, except start by
 entering this command:</p>
<pre>ssh linux.engr.ucsb.edu</pre>
 <p>Please follow the instructions above, and make sure that everything works properly.</p>

 <h3>Step 4: Create some directories</h3>
 <p>At the command prompt, we are going to type several commands to create folders
 (called &quot;directories&quot;) on Linux in which you can store your programs. The
 commands are shown in the box below&mdash;but first, a little explanation.</p>
 <p>Each of the <strong>cd</strong> commands shown below is a command to &quot;change
 directory&quot;&mdash;that is to move into a different folder on the hard drive. </p>
 <ul>
   <li>When you type <strong>cd</strong> by itself, it takes you to your
  'home directory'.</li>
   <li>cd followed by a directory name (e.g. <strong>cd cs8</strong>) moves you into
   a directory under the current one</li>
  </ul>
 <p>Each of the <strong>mkdir</strong> commands &quot;makes a new directory&quot;
 (i.e. a new folder). </p>
 <ul>
   <li>For example,<strong> mkdir cs8</strong> creates a new directory called cs8,
	inside the current directory.</li>
  </ul>
 <p>Each of the pwd commands &quot;prints the working directory&quot;,
 i.e. it tells you where you are on the hard drive.</p>
 <ul>
   <li>Your home directory is something like <strong>/cs/student/jsmith</strong>
 or <strong>/engr/student/mdiaz</strong></li>
   <li>Under that, you might have a directory cs8&mdash;that would show up as
 <strong>/cs/student/jsmith/cs8</strong>, or <strong>/engr/student/mdiaz/cs8</strong></li>
 </ul>
 <p>At the command prompt, type each of these commands. What you type is shown in bold.
 You should get back exactly the output shown, (except that the part in italics may be different&mdash;each user will have something different show up there.)</p>
 <pre>-bash-4.2$ <strong>cd</strong>
-bash-4.2$ <strong>pwd</strong>
/<em>cs</em>/<em>student</em>/<em>yourusername</em>
-bash-4.2$ <strong>mkdir cs8</strong>
-bash-4.2$ <strong>cd cs8</strong>
-bash-4.2$ <strong>pwd</strong>
/<em>cs</em>/<em>student</em>/<em>yourusername</em>/cs8
-bash-4.2$ <strong>mkdir lab00</strong>
-bash-4.2$ <strong>cd lab00</strong>
-bash-4.2$ <strong>pwd</strong>
/<em>cs</em>/<em>student</em>/<em>yourusername</em>/cs8/lab00
-bash-4.2$ <strong>cd</strong>
-bash-4.2$ <strong>pwd</strong>
/<em>cs</em>/<em>student</em>/<em>yourusername</em></pre>
 <h4>Checking if it worked</h4>
 <p>To see if it worked, you can use the file manager on the desktop. Drag any windows
 that might be covering up the &quot;Home&quot; icon
 on your desktop&mdash;it should be near the upper left hand corner of the screen.
 When you double click on this icon, it will bring up your home directory. You should
 see inside a folder called cs8. If you double click on that, you should see inside
 of it, a folder called lab00.</p>
 <p>Note that you could also use mouse clicks and menu options to create these folders,
 instead of the command line. If you have trouble with the command line, then for today,
 it is ok to do it that way. </p>
 <p>Eventually, though, we want you to learn some of the Unix commands 
  also&mdash;the reasons it is important to know both will become more clear 
  as you move deeper into the study of programming and Computer Science.</p>

 <h3>Step 5: Bring up the program called IDLE</h3>
 <p>The preliminaries are done&mdash;now we are ready to start saving files
for Python!</p>
 <p>IDLE is a piece of software that you use to interact with the Python programming
 language. As we are using Python version 3 in this class, we also use IDLE version 3.
 Type the following at the command prompt:</p>
 <pre>-bash-4.2$ <strong>idle3</strong></pre>
 <p>The window that appears should have the Python Command prompt (&gt;&gt;&gt;)
 in it.</p>
 <ul>
   <li>This is sometimes called the &quot;Python Command Prompt&quot; window.</li>
   <li>This is also called the &quot;Python Shell&quot; window.</li>
 </ul>
 <p>When you have the IDLE window up, you are ready for the next step.</p>

 <h3>Step 6: Save a file in IDLE</h3>
<p>In IDLE, select &quot;File=&gt;New Window&quot; to open a new &quot;untitled&quot;
 window for Python code.</p>
<p>When it comes up, click and drag the window by its title bar over to the right
 of your Python Shell window.</p>
<p>Then, open a web browser to the link below. </p>
<ul>
  <li>Hint: You may be able to use right-click (control-click on Mac), to open this link
  in a new window.</li>
</ul>
<p><a href="http://www.cs.ucsb.edu/~mikec/cs8/assignments/labs/lab00/zen.txt">http://www.cs.ucsb.edu/~mikec/cs8/assignments/labs/lab00/zen.txt</a></p>
<p>Go ahead and read it, but then "select all" of the text, "copy" it and "paste"
 it into the new &quot;untitled&quot; window.</p>
<ul>
  <li>Note: if the usual keystrokes for copy and paste are not working, try the
 menu options under &quot;Edit&quot; for copy and paste.</li>
  </ul>
<p>At the top of the file, type "Copied by: " followed by your name and, if another
student is working with you today, the other student's name on the same line as yours.
Make sure you type "Copied by:" exactly as shown, including capitalization.</p>
<p>You'll have to save the file. Save the file with the name zen.txt inside the
 cs8/lab00 folder you created in the previous step. </p>

<h3>Step 7. Submit your assignment using the turnin program on CSIL</h3>
<p>To submit your assignment, you need to bring up a terminal window on CSIL.</p>
<p>To start this process, bring up a terminal window exactly the way you did in
 Step 2.</p>
<p>Next, we use the cd command that we practiced earlier:</p>
<pre>-bash-4.2$ <strong>cd</strong> 
-bash-4.2$ <strong>pwd</strong> 
/<em>cs</em>/<em>student</em>/<em>yourusername</em> 
-bash-4.2$ <strong>cd cs8</strong> 
-bash-4.2$ <strong>pwd</strong> 
/<em>cs</em>/<em>student</em>/<em>yourusername</em>/cs8 
-bash-4.2$ </pre>
<p>When you are in inside your cs8 directory, you are ready for the turnin step.
 Note that your account must work to get credit.  If your account
 does not work, you must go to CSIL later to turn in the lab.</p>
<p>Type the following at the prompt:</p>
<pre>turnin Lab00@cs8c lab00</pre>
<p>Careful: that's an uppercase 'L' at the start, and lowercase 'l' later, and the class
 name is "cs8c" for the MW (Costanzo) section. You should be asked if you want to turn in
 this file. Respond &quot;yes&quot;, and then you should get a message indicating that your
 efforts were successful!</p>

<h3>Step 8. Log Out</h3>
<p>Actually, this is the final step of <em>every lab</em>, but we probably won't
 remind you again after this one.
In fact, you should do this every time you walk away from a lab computer, either
 in Phelps 3525 or CSIL.</p>
 <p>Here's how:</p>
 <ul>
   <li>Find the System Menu at the top of the screen.</li>
   <li>Select Log Out</li>
  </ul>
 
<table bgcolor="lightcyan" border="1" cellpadding="4"><tbody><tr><td>
   <strong>Second partner should now log in and redo Steps 2 through 8.</strong>
   <br>The first partner should not leave though: help your partner out. Things should
   go much more quickly and smoothly the second time through.
</td></tr></tbody></table>

<hr>

<h2>Evaluation and Grading</h2>
<em>Each</em> student must accomplish the following to earn full credit for this lab:
 <ul>
   <li>Turn in a complete and accurate Hw0 - your TA should have collected it earlier.</li>
   <li>zen.txt is complete, with "Copied by:" and your name, and is saved in ~/cs8/lab00/.</li>
   <li>zen.txt is turned in from your user account.
   <!--<br><b>Deadline for after-lab submission: Tonight at 11:59pm.</b>
      <br><i>Note that to be eligible for late turn-in with credit, you MUST have attended
          your entire lab period.</i>--></li>
 </ul>
 <p>You should try to complete this assignment by the end of the lab section.
  This first lab, however, will be accepted late without penalty from students who register for
  the class late, or anyone who needs extra help.</p>
<p><strong>Deadline for after-lab submission: Sunday, April 9 (11:59pm).</strong>
 Remember this deadline is lax for the first lab only. Later labs must be completed the
 same day they occur, and attendance in-lab usually is mandatory to receive any lab credit beyond
 homework points.</p>
 
<hr>
<blockquote>
<h3>After both partners finish the lab work above</h3>
<p>Normally this section of the labs will have optional challenges for you to work on after
completing the mandatory tasks. That is, if you finish the required work early, then we
want you to do additional work until the lab officially ends.</p>
<p>Are you one of the first pairs to finish? Then look around for classmates who might be
struggling, and ask them if you can help. After all of your classmates are either done or being
competently helped by someone else, then you may ask the TA to be excused. That is, today
you may leave early, but only after you are sure that nobody needs your help.</p>
</blockquote>

 <hr>

<h3>If your account doesn't work:</h3>
 <p>If you try to create a College of Engineering account, and it doesn't work, then
  send email to support@cs.ucsb.edu. In your email, </p>
 <ul>
   <li>cc your instructor and your TA on the email.</li>
   <li>Indicate that you are enrolled in CS8 </li>
   <li> Tell approximately what day you enrolled in the class on GOLD and 
     when you completed (or attempted) the form at
     <a href="https://accounts.engr.ucsb.edu/create/">https://accounts.engr.ucsb.edu/create/</a> </li>
  </ul>
 <p>Note: DO NOT include your password in your email to support. In fact, NEVER send your
  password through email, and NEVER tell anyone else your password, not even the support
  staff. Real support staff will NEVER ASK YOU FOR YOUR PASSWORD&mdash;not over email,
  and not in person. They won't need it to help you. </p>
 <p>If someone is asking for your password over email, it is a scam called a
 &quot;phishing attack&quot;&mdash;don't be fooled by these dastardly villains. </p>
 <hr>
 <p>Copyright 2009, Phillip T. Conrad, CS Dept, UC Santa Barbara. Permission to copy
  for non-commercial, non-profit, educational purposes granted, provided appropriate
  credit is given;  all other rights reserved. Adapted by Ziad Matni and Mike Castano for this quarter.</p>
