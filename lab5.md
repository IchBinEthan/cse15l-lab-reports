# Lab Report 5 -- Debugging

For this Lab Report, I cite Emi Van Cleave for collaboration on getting started with Part 1. Props to Emi. :)

## Part 1: Debugging

## Step 1: The Report

 `Edstem report. Student: Doe, Jonathan`
 
 
 
 `What environment are you using (computer, operating system, web browser, terminal/editor, and so on)?`

I am using Macbook Pro with M1, with Visual Studio Code as my IDE.

`Detail the symptom you’re seeing. Be specific; include both what you’re seeing and what you expected to see instead. Screenshots are great, copy-pasted terminal output is also great. Avoid saying “it doesn’t work”.`

I am looking at the code for Skill Demo 2 and I am trying to fix ``grade.sh``. I have not made much progress, since I am failing the test.

`Detail the failure-inducing input and context. That might mean any or all of the command you’re running, a test case, command-line arguments, working directory, even the last few commands you ran. Do your best to provide as much context as you can.`

Well, the code doesn't seem to work. I believe it has to do with the referencing of the `ListExamples.java`.
With the referencing of the file, the file says that the test does not pass. I need a quick solution!

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15lab5.edstemLE.png)
![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15lab5.edstemFail1.png)

However, my colleage Emmerz van Cleanex gave me advice to make sure that using the path would make the file pass the test. It did. Therefore, there must be something wrong with the implementation?

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15lab5.edstemPath.png)
![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15lab5.edstemPass.png)

## Step 2: The TA Response

Hello, John Doe! The implementation might not be proper. What if instead, you used a '$' in front?

## Step 3: The Student Response

Somehow (and this is ethan speaking too) the code still doesn't work. Even after putting the $ in front of ListExamples I was unable to achieve the goal. To confirm that the reference would work, I even tried to verify by typing `echo "ListExamples: $ListExamples".` This is even confirmed in the test! Maybe I had trouble cloning the file, but this part of the assignment remains unfinished. 

![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15lab5.edstemEdited.png)


![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15lab5.edstemFail2.png)
Here is me running the test. Something is still wrong because I keep getting 0/4. This line confirms the reference getting through to the path I want. 
![Image](https://ichbinethan.github.io/cse15l-lab-reports/cs15lab5.estemFail3.png)


... I really don't know what to say here.

### Step 4: The Information.

I was able to obtain a clone of the github repository through the write-up on EdStem. This was shortly after I finished Skill Demo 2 (yes. this is late. I know). I used the [link](inpttps://github.com/ucsd-cse15l-s23/grader-skill-demo2) provided to clone with the command `git clone`.

I used `vim` to find the issue and try to fix it. The bash inputs were sued for verification, and the specific command was `bash grade.sh` and the [link](https://github.com/ucsd-cse15l-s23/list-methods-corrected) in the write up to test it with.


## Part 2: Reflection

Honestly, this quarter was really tough. I struggled really badly this quarter, and I had a lot of personal issues. I have a lot of trouble integrating into the community of Computer Science. My take might be  negative, but I am grateful for making friends such as Melanie Haro and Emi Van Cleave, who have been in my group for many lab sections. Other than that, I think a break from this is long overdue. 
