__Cool Picture__: ![World Map](Image1.jpg)

```
Cool Link:
```

[My Index Page](https://henohyj.github.io/cse15l-lab-reports/index.html)



# Installing VS Code:

Google “VS Code”, find the official website, and download the .exe file of corresponding controlling system to your computer. Then click it and follow the steps to complete the installation.


# Remotely Connecting:

Type the command cs15lwi22zz@ieng6.ucsd.edu:~/, and remember to replace the “zz” with the correct letters of your account.

Then it should display something like this:

<<<<<<< HEAD
![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/1.png)

Then, type in your password of your account, it’s normal that you tap your keyboard but nothing shows up, just type in the password and press enter.

![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/2.png)
=======
![pic](report1 images/1.jpg)

Then, type in your password of your account, it’s normal that you tap your keyboard but nothing shows up, just type in the password and press enter.

![pic](report1 images/2.jpg)
>>>>>>> parent of 8507fea (Update lab-report-1-week-2.md)

If you see similar messages above, it means that you successfully connect to the remote server.


# Trying Some Commands:

<<<<<<< HEAD
![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/3.png)

![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/4.png)
=======
![pic](report1 images/3.jpg)

![pic](report1 images/4.jpg)
>>>>>>> parent of 8507fea (Update lab-report-1-week-2.md)

You can try playing around with some commands like me.


# Moving Files with scp:

Next, you will learn how to copy a file from your pc to the server, by using the “scp” command.

(Remember to use “exit” or Ctrl+D to return to your device)

<<<<<<< HEAD
![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/5.png)

And log back into the server to check the file:

![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/6.png)
=======
![pic](report1 images/5.jpg)

And log back into the server to check the file:

![pic](report1 images/6.jpg)
>>>>>>> parent of 8507fea (Update lab-report-1-week-2.md)

Now you can see I successfully copied a file “index.md” from my pc to the remote server


You can also run code on the server, just type in javac and java like on your pc:

<<<<<<< HEAD
![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/7.png)
=======
![pic](report1 images/7.jpg)
>>>>>>> parent of 8507fea (Update lab-report-1-week-2.md)

This WhereAmI.java is a file I previously put in, and it prints out some information about the device you are using.


# Setting an SSH Key:

You will find every time if you want to communicate to the server from your pc, it asks you to type in the password. By setting the ssh key can solve this inconvenience. 


If you are Windows system, please definitely follow what I did following:

<<<<<<< HEAD
![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/8.png)

Please directly copy the path from your explorer or it cannot correctly recognize the file path.

![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/9.png)
=======
![pic](report1 images/8.jpg)

Please directly copy the path from your explorer or it cannot correctly recognize the file path.

![pic](report1 images/9.jpg)
>>>>>>> parent of 8507fea (Update lab-report-1-week-2.md)


Then, you log back into the server to create a new directory by using the following command:
“mkdir .ssh”

Then go back on the client (your pc) to run this command

<<<<<<< HEAD
![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/10.png)
=======
![pic](report1 images/10.jpg)
>>>>>>> parent of 8507fea (Update lab-report-1-week-2.md)

# Optimizing Remote Running:

Now you can see that you are no longer need type your password every time to communicate with the server from the client:

<<<<<<< HEAD
![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/11.png)
=======
![pic](report1 images/11.jpg)
>>>>>>> parent of 8507fea (Update lab-report-1-week-2.md)


(You can also use semicolons to divide several commands that you want to run in the same line)

<<<<<<< HEAD
![pic](https://github.com/HenoHyj/cse15l-lab-reports/blob/main/report1%20images/12.png)
=======
![pic](report1 images/12.jpg)
>>>>>>> parent of 8507fea (Update lab-report-1-week-2.md)
