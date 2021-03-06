# CSE15L-LabReport1

## 1. Installing VScode
Go to the Visual Studio Code website [Link](https://code.visualstudio.com/), and follow the instructions to download and install it on your computer.
In this step, I showed that I have successfully downloaded the VSC app.

![Image](https://user-images.githubusercontent.com/103146938/162255778-9dd4eb08-623c-4d3e-b778-74558d00bca9.png)
## 2. Remotely Connecting
If you are using Windows, go to [Link](https://docs.microsoft.com/en-us/windows-server/administration/openssh/openssh_install_firstuse) which allows your computer to connect to others remotely. Then, look up your course account here [Link](https://sdacs.ucsd.edu/~icc/index.php). After setting this up, go to VSC, open a new terminal, and enter ssh `cs15lsp22zz@ieng6.ucsd.edu`, where you should substitute "zz" with your personal account letters.

After entering the password (although the characters are not shown), you will see something like:

![Image](https://user-images.githubusercontent.com/103146938/162259088-39b06b18-c5f2-48b6-83c6-ebda8edaa4eb.png)
That indicates that you have successfully connected to a remote computer.

## 3. Trying Some Commands
There are some commands that you can use to show some specifc things, such as `cd`, `ls`, `pwd`, `mkdir`, and `cp`. After doing `ls -lat`, I had all the things that might appear after `-l`, `-a`, and `-t`.

![Image](https://user-images.githubusercontent.com/103146938/162272598-e2145eb5-9bf9-4351-bfb0-61ae4497561f.png)

## 4. Moving Files with `scp`
1. Enter `exit` to exit the remote control and get back on the client end.
2. Create a new local file called "WhereAmI" storing the print statements that show the property of the different ends, and run it with `javac` and `java` command. At this point, you should see a directory list on your own client computer.
3. Enter `scp WhereAmI.java cs15lsp22avq@ieng6.ucsd.edu:~/` in the terminal, and the password as prompted.
4. Do the same `ssh cs15lsp22avq@ieng6.ucsd.edu` and the password to login to the ssh control.
5. Do `ls`, and you will find the "WhereAmI.java" in the list of files.
6. Run the commnads in step 2 again, but this time it would show the directory list on the remote computer.

![Image](https://user-images.githubusercontent.com/103146938/162275864-d29ae06b-43da-48ac-a575-719d4d017302.png)

## 5. Setting an SSH Key
1. Enter `ssh-keygen` on the client end.
2. The terminal gives you 
```
Generating public/private rsa key pair.
Enter file in which to save the key (/Users/vincent./.ssh/id_rsa): 
```
3. Keep pressing "enter" until you get the graph.
4. Enter `ssh cs15lsp22zz@ieng6.ucsd.edu` and the password.
5. Enter `mkdir .ssh` to make a new directory.
6. `exit` and get back on the client side.
7. Do `scp /Users/vincent./.ssh/id_rsa.pub cs15lsp22avq@ieng6.ucsd.edu:~/.ssh/authorized_keys` (for myself to copy and paste directly).
8. Then you should be able to login to ssh without password.

![Image](https://user-images.githubusercontent.com/103146938/162352125-8708fd01-0996-4cbe-b8e4-4f388bfd7550.png)


## 6. Optimizing Remote Running
At this step, we will be able to do commands directly after `ssh` if we put them in `""`.
![Image](https://user-images.githubusercontent.com/103146938/162353086-693cb9cd-6fa4-465a-afc3-994a11c7f606.png)

