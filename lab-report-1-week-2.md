__Cool Picture__: ![World Map](Image1.jpg)

```
Cool Link:
```

[My Index Page](https://henohyj.github.io/cse15l-lab-reports/index.html)



# Installing VS Code:

Google “VS Code”, find the official website, and download the .exe file of corresponding controlling system to your computer. Then click it and follow the steps to complete the installation.

This is what Visual Studio Code's official website looks like:
![pic](report1 images/0.png)

Here's the link for downloading Win64x version VS Code:
[VS Code Download](https://code.visualstudio.com/docs/?dv=win64user)


# Remotely Connecting:

Type the command 
```
ssh cs15lwi22zz@ieng6.ucsd.edu:~/
```
and remember to replace the “zz” with the correct letters of your account.

Then it should display something like this:

![pic](report1 images/1.png)

Then, type in your password of your account, it’s normal that you tap your keyboard but nothing shows up, just type in the password and press enter.

![pic](report1 images/2.png)

If you see similar messages above, it means that you successfully connect to the remote server.


# Trying Some Commands:

You can try playing around with some commands like me:
```
ls 
mkdir hello
cd ..  or  cd ~
cp filename hello
```
![pic](report1 images/3.png)

![pic](report1 images/4.png)


# Moving Files with scp:

Next, you will learn how to copy a file from your pc to the server, by using the “scp” command.

(Remember to use ```exit``` or Ctrl+D to return to your device)
```
scp filename cs15lwi22zz@ieng6.ucsd.edu:~/
```
![pic](report1 images/5.png)

And log back into the server to check the file:

![pic](report1 images/6.png)

Now you can see I successfully copied a file “index.md” from my pc to the remote server, by using ```ls``` command to check it.


You can also run code on the server, just type in javac and java like on your pc:
```javac WhereAmI.java ```   ```java WhereAmI```
![pic](report1 images/7.png)

This WhereAmI.java is a file I previously put in, and it prints out some information about the device you are using.
(You may check the function of the semicolon used in here at the last step _Optimizing Remote Running_)


# Setting an SSH Key:

You will find every time if you want to communicate to the server from your pc, it asks you to type in the password. By setting the ssh key can solve this inconvenience. 


If you are Windows system, please definitely follow what I did following:
First, type in ```ssh-keygen``` in the terminal

![pic](report1 images/8.png)

Please directly copy the path from your file explorer, so it can correctly recognize the file path.
(I have this ```Overwrite (y/n)?``` notice because I'm re-doing this process, if you are setting it for the first time, you would not see such information)

Then it will ask you to set a passphrase, follow its instruction and type your own password twice. 
(The password content won't show up like when you are connecting to the remote server)

Here's the extra steps for Windows system:

Type in the following commands in sequence: 

```Get-Service ssh-agent | Set-Service -StartupType Manual``` 

```Start-Service ssh-agent``` 

```Get-Service ssh-agent``` 

```ssh-add C:\Users\Username\.ssh\id_rsa```

and type in the password you just set when it asks you for the passphrase

![pic](report1 images/9.png)

Then, you log back into the server to create a new directory by using the command ```mkdir .ssh```

Then go back on the client (your pc) to run this command ```scp C:\Users\Username\.ssh\id_rsa.pub cs15lwi22zz@ieng6.ucsd.edu:~/.ssh/authorized_keys``` to copy the _public_ key to the ```.ssh``` directory of your user account on the server

![pic](report1 images/10.png)

Thus, you should be able to communicate with the remote server when you are still at your device(client) without typing the password every time.

# Optimizing Remote Running:

Now you can see that you are no longer need type your password every time to communicate with the server from the client.
Try this command on your own device(the client) ```scp filename cs15lwi22zz@ieng6.ucsd.edu:~/``` 

![pic](report1 images/11.png)

You'll surprisingly find that you don't have to type in the password this time, which is the same when you run ```ssh cs15lwi22zz@ieng6.ucsd.edu:~/```

Let's count keystrokes to prove that we do save the time after setting the ssh key:
Originally, running the command ```ssh cs15lwi22@ieng6.ucsd.edu "ls"``` needs 33 keystrokes , 
plus the keystrokes of typing in the password. For me, my password requires 9 keystrokes. 
Adding them together with 2 presses of "enter", the result will be total 44 keystrokes to complete the whole command of checking the files in the root directory.

After we successfully setting up the ssh keys, the total key strokes will only be 34 keystrokes, which is typing the command ```ssh cs15lwi22@ieng6.ucsd.edu "ls"``` with a press of the enter key. We do save time for 10 keystrokes.
If you sometimes mistype your password, you will waste more time to type in the correct password again. Therefore, we can see that setting up ssh keys really help optimize remote running experiences.

You can also use semicolons to divide several commands that you want to run in the same line:
```cp WhereAmI.java OtherMain.java; javac OtherMain.java; java WhereAmI```

![pic](report1 images/12.png)
