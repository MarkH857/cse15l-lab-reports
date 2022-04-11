# A tutorial on how to log into a course-specific account on ieng6

## **Step 1: Installing VS Code** 
Go to VS Code website to down load VS Code. [Link is here.](https://code.visualstudio.com/)  
Open the VS Code after installation and you should be able to see a fresh window similar to the following picture:  
![image](VS_Code_Homepage.png)
---

## **Step 2: Remote Connection**  
1. Open a new terminal in VSCode. Then enter the following command:  
`$ ssh cs15lsp22zz@ieng6.ucsd.edu`  
with zz replaced by the letters in your course-specific account.
2. Type yes to the message you get (the message should look like  
`The authenticity of host 'ieng6.ucsd.edu (128.54.70.227)' can't be established.`) and press enter.
3. Type your password afterwords and you should get a page similar to the following:  
![image](Successful_Login.png)  

---

## **Step 3: Some useful commands**
You can try some commands that enables you to do a variety of cool operations. Here are some examples:  
![image](Some_Commands.png)

---

## **Step 4: Moving Files with `scp`**
1. Create a java file on your computer, for example a WhereAmI.java file(**Not on the remote server!**)).
2. Run the following command in the terminal from the directory where you made the file:  
`scp WhereAmI.java cs15lsp22zz@ieng6.ucsd.edu:~/`
3. Log back into the remote server and you should be able to see your file (here it is WhereAmI.java) using the `ls` command.
![image](Copying_File_1.png)
![image](Copying_File_2.png)

---

## **Step 5: Setting an SSH Key**
1. Create a private key and a public key stored in the .ssh directory in your personal computer.
![image](SSH_Keys1.png)
2. Copy the public key to the remote server.
![image](SSH_Keys2.png)
![image](SSH_Keys3.png)
3. You should be able to login to the remote server without typing out the password after the aforementioned steps.
---

## **Step 6: Optimizing Remote Running**
1. You can directly type a command at the end of an `ssh` command to run it right after login instead of loggin in first and then run the command.
![image](Optimizing_Command1.png)  
2. You can use semicolons to run more than one command at a time.
![image](Optimizing_Command2.png)
