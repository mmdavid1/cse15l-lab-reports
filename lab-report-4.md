<h1>Lab Report 4<h1>
<h2><strong>Part 1</strong></h2>

<p>I am going to be showing the commands to insert the print statement before the File[] paths statement in DocSearchServer.java (assume you have the DocSearchServer.java file opened in vim)</p>
<br>

<ol>
<li>   
        
        <esc>

This ensures you are in normal mode in vim, which is needed for the next commands.
<li>
        
        /File[]

<li>

        <enter>

![finding-file](findingfile.PNG)

As  you can see at the first line, the cursor has now moved to the first occurence of "File[]", which is where we want the cursor to be (note that the find function is case sensitive)

<li>
        
        k 

![moving-up](k.PNG)

The k key is going to move the cursor up one line, which we need to happen for the next command we will be using. (note that we pressed k in normal mode, so that it moved the cursor up one line)

<li>

        o
![creating-new-line](o.PNG)

The o character (in normal mode) creates an empty line below the current line and also puts vim into edit mode, which we need to do to insert the print statement (as seen in the image, there has now been a line above the File[] line)

<li>
        
        <tab> + 4 spaces 
![tabing](tab.PNG)
    
Now that we are in insert mode and the cursor is on the line we want to insert, we need to move the cursor to the exact space we want to type at so that the file is still formatted correctly. After doing this, the cursor will be exactly where we want it to be to start typing <b>(total number of keystrokes so far is 10)</b>

<li>

        System.out.println(f.toString() + “is a directory”);
![writing-print-statement](print.PNG)

Because we were in the correct spot with the cursor and we were in insert mode, we were simply able to type the line of code we wanted to insert (I counted this whole command as 1 key stroke, because if we count the individual number of keys it took to type this it is over 50)

<li>
       
        <esc>
hitting the esc character takes us out of insert mode

<li>

        :wq<Enter>
![file-saved](wq.PNG)

:wq will write and quit the vim file, so it will save the changes you have made and quit vim, which is what we want now that we have made the changes needed (Image shows my current directory outside vim)

The total number of keystrokes it took to complete this sequence was 13
<br>
<h2><strong>Part 2</strong></h2>

<strong>Report: </strong>

---
1. Option 1 took me 47 seconds to complete, the longest part being having to scp the files over. No difficulties came up
2. Option 2 took me 57 seconds. I was already familiar with the exact commands to complete this task becasue of part 1, so there was no difficulties

<br>
<strong>Questions: </strong>

---
1. I would prefer option 1 if I had to work remotely, and the reason is that I feel like I have more control when I am editing files on my local computer than on the remote computer, because I am more used to it and can troubleshoot more easily, for example VScode will tell me if there are any compile errors, formatting errors, etc, which is helpful because I can ensure I am pushing accurate code to the remote before pushing anything.
2. If the task involved a lot of testing code and my computer had the capabilites of testing that code without running into errors (caused by the limits of my computer), I would rather use my local environment to code and edit the code. However if for some reason my computer couldn't handle the testing, then it would be convenient to use the remote.
 

