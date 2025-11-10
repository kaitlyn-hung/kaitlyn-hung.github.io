# Fundamental Linux Commands

### Purpose
Demonstrates my proficiency with essential Linux commands and navigation techniques commonly used in cybersecurity environments. Mastery of the Linux command line enables security analysts to efficiently manage files, investigate systems, and perform security operations with precision. 

### Skills Demonstrated
+ Install and manage applications on a Linux operating system
+ Navigate, manage, and analyze files 
+ Return specific information by combining the ```grep``` command and piping
+ Create and remove directories
+ Edit files with the nano text editor
+ Add new users, add user to a group, change user permissions on files, delete a user

---

### 🐧 Install and manage applications on a Linux operating system 
The APT package manager must be installed in order to manage applications. When APT is installed, ```apt``` displays basic usage information when run, including the version information and a description of the tool. 

Install tcpdump and Suricata. 
```bash
sudo apt install suricata
```
```
sudo apt install tcpdump
```
Note: The ```apt install``` and ```apt remove``` commands are used with the sudo command because elevated privileges are required to install and uninstall software in Linux.

List the installed applications using the APT package manager. 
```
apt list --installed
```
Resulting output confirms both applications have been successfully installed.  
<img width="746" height="100" alt="Screen Shot 2025-10-21 at 9 49 47 PM" src="https://github.com/user-attachments/assets/5eef80de-46d6-4ced-8181-cef2a4ab4dff" />



### 🐧 Navigate, manage, and analyze files 
Current directory is /home/analyst displayed using the ```pwd``` command. ```ls``` displays the names of the files and directories in the current working directory. To navigate to one of these files or directories, such as the **reports** directory, ```cd reports``` or ```cd /home/analyst/reports``` is used.  

Navigate to the Q1_added_users.txt file within the **reports** directory. 
```
cd Q1_added_users.txt
```

Display the contents of the file Q1_added_users.txt file within the **reports** directory. ```cat``` command prints the contents of a file to the shell. 
```
cat Q1_added_users.txt
```

Display only the first 10 lines of the file. 
```
head Q1_added_users.txt
```

Display only the first 8 lines of the file.
```
head -8 Q1_added_users.txt
``` 


### 🐧 Return specific information with the ```grep``` command
In the **server_logs.txt** file, return all lines containing the text string **error**. Note: ```grep``` command returns a list of the lines that match the second argument.  
```
grep error server_logs.txt
```

The above example returns a **list of lines** that contain the search string within a file. Now, we'll look for all the **files** within a directory that contain the search string. Piping is used to input the result of the first command to the second. 

Look for files in the current working directory that contain the string **error**. 
```
ls | grep error
```


### 🐧 Create and remove directories
Create a new directory called **logs** in the **/home/analyst** directory. 
```
mkdir logs
```

Remove the **logs** directory. 
```
rmdir logs
```



### 🐧 Edit files with the nano text editor
Create an empty file called **tasks.txt** in the current working directory. 
```
touch tasks.txt
```

Using the nano text editor, add text to the newly created file. Pressing CTRL+X exits the editor. 
```
nano tasks.txt
```




### 🐧 Add new users, add user to a group, change user permissions on files, delete a user
Add a user called **researcher2** to the system. Add the user to the **research_team** group in another step. 
```
sudo useradd researcher2
```
```
sudo usermod -g research_team researcher2
```

Do both tasks in one step. 
```
sudo useradd researcher2 -g research_team
```

Make the user the owner of **project_r.txt** that is currently owned by researcher1. 
```
sudo chown researcher1 /home/researcher1/projects/project_r.txt
```

Delete the user **researcher2**. 
```
sudo userdel researcher2
```
Note: When you create a new user in Linux, a group with the same name as the user is automatically created and the user is the only member of that group. After removing users, it is good practice to clean up any such empty groups that may remain behind.  
Instead, delete the group.
```
sudo groupdel researcher2
```




