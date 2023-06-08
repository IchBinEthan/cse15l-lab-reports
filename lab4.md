# Lab report 4 -- Github and the Command Line

### Step 4: Logging into ieng6.

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15Lab4.4.png)

I typed out `ssh cs15lsp23gs@ieng6.ucsd.edu` to initiate login

Then I used `<enter>` `<password>` `<enter>` where `password` refers to my password. I was able to log in.


### Step 5: Clone your fork of the repository from your Github account.

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15Lab4.5.png)

I typed out `git clone` `<command>v` `<enter` where I copy-pasted the [link](https://github.com/ucsd-cse15l-s23/lab7) to the repository. I was able to clone it onto the remote server.


### Step 6: Run the tests, demonstrating that they fail

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15Lab4.6.1.png)

I typed out `cd lab7` to change the directory to that of lab7. I typed out `bash test.sh` and then it gave me the results on the command line. The results in the picture here show that after running the test, I get a failure message.


### Step 7: Edit the code file ListExamples.java to fix the failing test.

In this case, I needed to open `vim`.

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15lab4.E.png)

I opened `vim` by typing `vim ListExamples.java` then `<enter>`. From then on, I was able to have access to the file. It prompted me to type `E` to edit, and then now I had access to edit. 


![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15Lab4.7.1.png)

Here is the location of where the change needed to happen. For edsiting, I then pressed `<down>`  key 4 times to go down 4 lines, then `<right>` 9 times to go accross 9 characters to where I needed to edit. I then changed the character to 2 by pressing `2`, then `<right>` then `<backspace>`. The result of this is in the bottom of these two pictures.


![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15Lab4.7.2.png)

To finish, I pressed `<escape>` to exit editing. Then, I typed `:wq` then `<enter>` to save file, then quit and return to command line. 

### Step 8: Run the tests, demonstrating that they now succeed.

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15Lab4.8.png)

I then reran the test by typing `bash test.sh` again and then `<enter>` to execute. 

### Step 9: Commit and push the resulting change to your Github account.

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15lab4.9.1.png)

So for this, I had to run the 4 different commands. I first ran `got add ListExamples.java` and then pressed `<enter>` to update the file for committing.

I then checked the status by writing `git status` and `<enter>` to make sure it worked. Then I committed the changes by typing `git commit -m` then my comment `:44 edited typo`. At this point everything seemed to be working fine.

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15lab4.9.2.png)

Then at here, I tried to push by writing `git push` then the link to the repository. I signed using my ID `IchBinEthan` and using an accesss tokem. However, I ran into this error. It was very confusing as to what went wrong. At the time of writing this issue did not get resolved. I believe I tried executing correctly, though this is the situation.
