READ THESE IMPORTANT CONDOR TIPS/FACTS (PLEASE)

1) All you need to run your code on the condor clusters is a .job file and .sh file.

2) The .job file tells condor important information about where you .sh file is located (we will get to that), where to save condor output, the memory necessary for your simulation, etc.

3) Note that the .job file asks for an email address. DO NOT USE A DUMMY EMAIL ADDRESS (unless you enjoy Brookhaven emails at 4am telling you their condor people are very frustrated with mail error messages)

4) The .job file should point to the correct .sh file, which...

5) The .sh is responsible for setting up an environments, 'cd-ing' into the directory of your code (a .C file for instance)

6) The .sh file is pretty much what you would normally type into your command line to get your code running. Anything you write in the .sh is equivalent to you running it line by line in the command line. You are essentially telling a supercomputer at BNL to type what you want to be typed/executed line by line

7) When you're all set, running "condor_submit sample.job" will send the instructions to one of any available clusters (you may need to wait a few minutes for it to find one)

8) You can keep track of your job's process by looking at the .out file created. For instance, if running a program which analyzes events one at a time, you can output the event number in the .C file with a "cout" statement which would appear in the supercluster's 'terminal'. This is fed into the .out file

9) When its all done, the .log file should display that the simulation was completed. 
