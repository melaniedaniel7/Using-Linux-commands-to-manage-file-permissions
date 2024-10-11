# File permissions in Linux
Screenshots of your commands 
Explanations of your commands
Details on using chmod to update file permissions
Details on checking file permissions with ls -la
Details on interpreting the 10-character string that represents file permissions
Details on hidden files and directories

### Project description
Describe what you accomplish through Linux commands.
In the Project description section, give a general overview of the scenario and what you accomplish through Linux. Write two to four sentences.
In this activity I acted as a security professional at a large organization. In this scenario I primarily work with the research team.
I use Linus commands to help keep the system secure by implementing the principle of least privilege, managing authorizations and permissions.


### Check file and directory details
Describe the command you can use to check permissions and indicate the current permissions.
The Linux command to check permissions is `ls -l` indicated below by green. The current permissions are represented by a 10-character string which is indicated below by red. The file and directory names are indicated below by blue.

![screenshot 1](https://github.com/melaniedaniel7/Using-Linux-commands-to-manage-file-permissions/blob/4fa62265862da01e3710977be289daa27d1e484e/Screenshot%202024-10-11%20at%2013.17.04.png)

### Describe the permissions string
write a short description that explains the 10-character string in the example. 
You should describe what the 10-character string is for and what each character represents.
In the 10-character string the file or directory is indicated by character 1, the user group permissions are indicated by characters 2-4, the group permissions is represented by characters 5-7, and the other users permissions are represented by characters 8-10.
There are three types of permissions for each of the three types of owners mentioned above. 
The three types of permissions in Linus are:
- read `r`
- write `w`
- execute `x`
The current permissions indicate that:
- The `drafts` is a directory `d` where the user has read `r`, write `w`, and execute `x` permissions. The group has execute `x` permissions and the other users have no permissions.
- The `project_k.txt` is a file `-` where the user, group, and other users all have read `r` and write `w` permissions.
- The `project_m.txt` is a file `-` where the user has read `r` and write `w` permissions. The group has write `w` permissions and the other users have no permissions.
- The `project_r.txt` is a file `-` where the user and group both have read `r` and write `w` permissions. The other users only have read `r` permissions.
- The `project_t.txt` is a file `-` where the user and group both have read `r` and write `w` permissions. The other users only have read `r` permissions.

### Change file permissions


### Change file permissions on a hidden file


### Change directory permissions


### Summary
In the Summary section, provide a short summary of the previous tasks and connect them to the scenario. Write approximately two to four sentences.
Your task is to examine existing permissions on the file system. You’ll need to determine if the permissions match the authorization that should be given. 
If they do not match, you’ll need to modify the permissions to authorize the appropriate users and remove any unauthorized access.
