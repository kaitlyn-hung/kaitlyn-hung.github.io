# Configuring Authorization using Linux Commands

### Purpose
Use Linux commands to configure authorization. Authorization is the concept of granting access to specific resources in a system. Without authorization, any user could access and modify all files belonging to other users or system files- a major security risk. 

### Skills Demonstrated
+ Examine file and directory permissions
+ Change permissions on files/directories

---
## Tasks
1️⃣ **Check the user and group permissions for all files in the projects directory.**

2️⃣ **Check whether any files have incorrect permissions and change the permissions as needed.**

3️⃣ **Change file permissions on a hidden file.**

4️⃣ **Change directory permissions.**  

---
## Results
#### Task 1️⃣: Check the user and group permissions for all files in the projects directory. 
Navigate to the **projects directory** from current directory /home/researcher2. 
```bash
cd project
```

List the contents and permissions of the projects directory.
```bash
ls -l
```
Results: The 10 characters at the beginning of each entry indicates the file type and the read, write, and execute permissions for user, group, and other. The second block of text is the user who owns the file. The third block of text is the group owner of the file.   
Here, line 2 represents a directory that the user has read, write, execute permissions, the group has execute permissions, and other has none. The user owner is researcher2 and the group owner is research_team.     
<img width="617" height="101" alt="Screen Shot 2025-10-21 at 6 39 32 PM" src="https://github.com/user-attachments/assets/8ed2f9df-9f04-4b01-8c84-462d2ae6f96a" />  




#### Task 2️⃣: Check whether any files have incorrect permissions and change the permissions as needed. 
In the expanded directory listing from the step prior, do any of the files have write permissions for the owner type of other? 
Yes. project_k.txt has write permissions for the owner type of other. 

Remove write permissions from the owner type of other from the file identified.
```
chmod o-w project_k.txt
```
In the chmod command, u sets the permissions for the user who owns the file, g sets the permissions for the group that owns the file, and o sets the permissions for others.  


Remove read or write permissions from the group to project_m.txt file. 
```
chmod g-r project_m.txt
```    
<br>


#### Task 3️⃣: Change file permissions on a hidden file. 
Determine if there are hidden files. 
```
ls -la
```
Project_x.txt is hidden file. User has read and write permissions. Group has write permissions.  

Change the permissions of the file .project_x.txt so that both the user and the group can read, but not write to, the file.
```
chmod u-w,g-w,g+r .project_x.txt
```  
<br>

#### Task 4️⃣: Change directory permissions.
Only the researcher2 user should be allowed to access the drafts directory and its contents. Currently, the user and group have execute permissions and therefore have access to the drafts directory. Therefore, execute permissions for the group must be removed from the drafts directory.
```
chmod g-x drafts
```  
---
### Final Thoughts
Through this project, I learned how to further interact with the Linux operating system using the chmod command to manage authorization of files and directories. These skills are essential for a security analyst because they strengthen my ability to work efficiently in a command-line environment, locate and analyze critical information, and manage system permissions to maintain security and integrity in a Linux-based system.

Previously, I practiced navigating and managing files, creating and removing directories, copying and editing files with the Nano text editor, and using commands like grep and piping to search for and extract specific information. 




