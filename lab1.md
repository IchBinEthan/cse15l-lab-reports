# Lab Report 1

Hi friends of CSE 15L! This is a tutorial for all of you to log into a course-specific account on ieng6.

## Step 0 -- Register for the account.
Have an ieng6@ucsd.edu account to begin with. Please make sure you have one to connect with; 
If not, ask your TA for help in registering. 

## Step 1 -- Install Visual Studio code. 

We can do this by going onto https://code.visualstudio.com/ and clicking the link to download the application based on the operating system you are using. For instance, I am a mac user (yeah, yeah, I know!) so I downloaded the app suitable for my mac.

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cse15Lab1step%201.png)

## Step 2 -- Remotely Connect.

Before starting, there is an extra step for any Windows user. They must need to get 'git' for Windows which proivdes some useful tools: Link to the package can be found [here](https://ucsd-cse15l-s23.github.io/week/week1/#week-1-lab-report:~:text=tools%20we%20need%3A-,Git%20for%20Windows,-Once%20installed%2C%20use). After installing, they can set the default terminal to use the 'git bash' in the app.

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cse15Lab1step2.png)

We start by opening a terminal and typing the command 'ssh' then typing in our email to log in. Recall that the email address for the course-specific account is the username + "@ieng6.ucsd.edu". For instance, my username is "cs15lsp23gs", therefore I type the following: "ssh cs15lsp23gs@ien6.ucsd.edu".

This is to connect to the server, which will then give us a prompt to continue connecting. It will then ask us to unput your password. Once given, we should be able to connect remotely to the server!

## Step 3 -- Run Commands! 

We are able to run commands into the terminal after logging in. Use some useful commands that are provided in the write-up for the lab, or the ones in the class lectures! Here are some examples of me running code.

Here are some examples for codes to run:
```
{cd ~
cd
ls -lat
ls -a}
```

* I tried `ls -lat` which prints out a list of things in the current directory, with extra information. This is displayed in a long format, showing hidden files, and sorted by time. 
* I tried `ls -a` which prints out all the hidden files of the current directory.

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cse15Lab1step3.png)
