# File permissions in Linux

Disclaimer: This project was created as part of my learning journey through the Google Professional Cybersecurity Certificate offered on Coursera. Some activities and content within this project were provided by the course as part of my coursework. All credit for such content belongs to Google and Coursera, and I acknowledge their role in supporting the completion of this project.

### Project description
In this activity I acted as a security professional at a large organization. In this scenario I primarily work with the research team.
I use Linus commands to help keep the system secure by implementing the principle of least privilege, managing authorizations and permissions.
In this activity I examined existing permissions on the file system, I determined if the permissions match the authorization that should be given, and I modified the permissions to authorize the appropriate users and remove any unauthorized access.

### Check file and directory details
The Linux command to check permissions is `ls -l` indicated below by green. The current permissions are represented by a 10-character string which is indicated below by red. The file and directory names contained within the current working directory called projects are indicated below by blue.

<img src="https://github.com/melaniedaniel7/Using-Linux-commands-to-manage-file-permissions/blob/4fa62265862da01e3710977be289daa27d1e484e/Screenshot%202024-10-11%20at%2013.17.04.png" width="600" />

### Describe the permissions string
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
The organization does not allow others to have write access to any files. 
Based off the image below the file `project_k.txt`, indicated by green, needs to have its write permissions modified. 
The Linux command to modify permissions is `chmod`. The Linux command to remove write permissions for other users in this file is `chmod o-w project_k.txt`. This is indicated by purple. The Linux command `ls -l` is used to check that these permissions were modified successfully. The result is indicated by pink.

<img src="https://github.com/melaniedaniel7/Using-Linux-commands-to-manage-file-permissions/blob/eb218cffd4a87b567ed8a665873cc6b5ed37374a/Screenshot%202024-10-11%20at%2014.13.15.png" width="600" />

### Change file permissions on a hidden file
The research team has archived .project_x.txt, which is why it’s a hidden file.
The Linux command `ls -la` displays hidden files. This command is indicated by blue in the image below.
The organization does not want this file to have write permissions for anyone, but the user and group should be able to read the file. 
The hidden file `.project_x.txt` currently has read permissions for the user and write permissions for both the user and the group. The period `.` before `.project_x.txt` indicates that this file is hidden. This is indicated by red.
The Linux command `chmod u-w,g=r .project_x.txt` will correct this error to the appropriate permissions and authorization for the types of owners. This is indicated by pink.
The Linux command `ls -la` is used once again to check that the correction was successful. The result is indicated by green.

<img src="https://github.com/melaniedaniel7/Using-Linux-commands-to-manage-file-permissions/blob/29f7f5a39e7a73df9ff5407311b18cca924efca1/Screenshot%202024-10-11%20at%2014.42.55.png" width="600" />

### Change directory permissions
The files and directories in the projects directory belong to the researcher2 user. Only researcher2 should be allowed to access the drafts directory and its contents. The Linux command `ls -l` displays permissions to files and directories. This is indicated by green. The image below shows that currently the group has execute permissions. This is indicated by red.
The Linux command `chmod g-x drafts` will modify this so that the correct permissions and authorizations are in place. This is indicated by purple.
The Linux command `ls -l` is used to check if the corrections were successful. The result is indicated by blue.

<img src="https://github.com/melaniedaniel7/Using-Linux-commands-to-manage-file-permissions/blob/9dc80bb137881049805d29f7ba852077c884b480/Screenshot%202024-10-11%20at%2015.10.16.png" width="600" />

### Summary
In this activity I checked file and directory details. I examined permissions useing the `ls -l` Linux command, I explained the 10-character string with an example of various permissions for the three types of owners, I determined if permissions matched the authorization they should be given, and if they did not I modified the permissions to authorize the appropriate users and remove any unauthorized access using the `chmod` Linux command for both normal and hidden files. Finally, I changed the draft directory permissions so that only researcher2 would be allowed to access the drafts directory and its contents using the `chmod` Linux command.
