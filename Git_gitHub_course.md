# **Udemy Git/GitHub Course**
**Important message up top** - EVERYTHING is stored as public information, history and all, online for the world to see. NEVER store sensitive info.

[link to course](https://www.udemy.com/course/git-and-github-crash-course-creating-a-repository-from-scratch/)

## **Vocabulary**
- repo (repository) - A place to store your code
- clone - download a file on github onto our computer so that we may make changes to it. It's just a fancy developer term for "copying"
- stageing - preparing a file before committing it to GitHub.
- Committing - Sending/Uploading a file.
- Push - send the code somewhere else.
- Local - Refering to something on your computer
- Fork - clone a repository into your own account on your local device.

**Command Line Vocab**

- ls: Displays the names of files and directories in the current directory.
- ls -la: Displays a detailed list (long format) of all files and directories, including hidden ones, with additional information such as permissions, ownership, size, and modification date.
    - Using ls -la gives you a more comprehensive view of the contents of a directory, which can be especially useful for understanding file permissions, ownership, and seeing hidden files that ls alone would not display.
- git log - delivers a ton of information about the history of the current project.

### **Course info**

This course will heavily be using the comand line. When you're on a server uploading code, there is no user interface tools, it's all command line.
//downloaded git through the terminal.

- Note: Whenever naming directories or files, use underscores as spacers. This prevents future issues as dashes and spaces can interfere with the code somehow...

On GitHub you can find a repository and clone it all thru the command line.
1. Go to github and copy the URL of the file you'd like to clone.
2. in the command line go to the directory you'd like to work with (in this case I made a new directory called websites [cd Desktop/coding, mkdir Websites])
3. You then type git (execute a git command), clone (the git command), then paste in the copied URL.
4. Optional command - enter the name of a directory you'd like to clone the URL into

![alt text](<Screenshot 2024-05-21 at 3.40.53 PM.png>)
Met with a message that I've cloned an empty repository.

* If you make any updates on Git, it does not immediatly get published in the cloud. Not how it works.

Add a markdown file into the repository. In my case I used:

- Joes-MacBook-Air:Websites j.chirchirillo$ cd Optional1

- Joes-MacBook-Air:Optional1 j.chirchirillo$ touch README.md

- Then edited the README.md file in VSC to display simple text.

- Staged the file by entering: "git add README.md" 
- The terminal returned with "Joes-MacBook-Air:Optional1 j.chirchirillo$" Checked work by entering: "git status" and the terminal retuned a list of changes to be committed (AKA the STAGED files) as well as some untracked file![alt text](<Screenshot 2024-05-21 at 4.24.08 PM.png>)s.

- After staging, but before committing, you can add a message.
    - git commit -m "Hello, this is my Initial commit" (-m prepares a message inside "" because the message is a string).
    ![alt text](<Screenshot 2024-05-21 at 4.29.59 PM.png>)

Check progress with "git status" results in nothing being in the changes to be committed. Success!

- If you go to github and refresh the page, there will be no changes. We did not commit it yet.

- We can truly commit the file be entering "git push origin master"
    - git(execute git command)
    - push (literally pushin the file somewhere else)
    - origin (which branch)
    - master (the main branch, the default code/repo you see on the github main page)
    -//you may be prompted to enter your github username and password.

//cant get it to work. keeps responding with:
 fatal: not a git repository (or any of the parent directories): .git
 // kept troubleshooting with help of chatgpt and it's just not working. Very frusterated.

 * Assuming this works, when you reload the Github page you should see your repository now had a file in it.
    * Note: there will be a message that says "initial commit" this is a tmestamp of when it was committed on your computer, NOT when it was pushed to Github. This keeps track of your `local work` (what's on your computer.)

**Making a change to a committed repository**

1. Make an edit to the original file.
2. In the terminal enter: git status
    - You should see a note about the file being modified and/or an untracked file.
    ![alt text](<Screenshot 2024-05-22 at 10.15.31 AM.png>)
3. In the command line enter: git add "file name to uploaded.example"
4. When you enter git status, it will have updated to :"changes to be committed"
![alt text](<Screenshot 2024-05-22 at 10.18.07 AM.png>)

5. (optional) You can enter: git diff README.md(the file in question) and you will be able to see the contents of the file in addition to if it is a second change.

Git will always record all stages of your code. So if you really beef it you can always find a past draft.

//Update: I got it to work with all but the last step. my previous error was from the inital git clone http address did not end with ".git". Trying it again got to the entering credentials stage. Still did not work because I do not have an SSH key setup.