#!/bin/bash
0. Create a script that switches the current user to the user betty.
0-iam_betty
su betty


1. Write a script that prints the effective username of the current user.
1-who_am_i
whoami


2. Write a script that prints all the groups the current user is part of.
2-groups
groups


3. Write a script that changes the owner of the file hello to the user betty.
3-new_owner
#!/bin/bash
chown betty hello

.
4. Write a script that creates an empty file called hello
4-empty
touch hello


5. Write a script that adds execute permission to the owner of the file hello.
5-execute
chmod u+x hello


6. Write a script that adds execute permission to the owner and the group owner, and read permission to other users, to the file hello.
6-multiple_permissions
chmod u+x, g+x, o+x hello

7.Write a script that adds execution permission to the owner, the group owner and the other users, to the file hello
7-everybody
chmod ugo+x hello

8. Write a script that sets the permission to the file hello as follows:
    • Owner: no permission at all
    • Group: no permission at all
    • Other users: all the permissions

8-James_Bond
chmod 007 hello

9.Write a script that sets the mode of the file hello to this:
 9-John_Doe
chmod 753 hello

10. Write a script that sets the mode of the file hello the same as olleh’s mode.
    • The file hello will be in the working directory
    • The file olleh will be in the working directory
10-mirror_permissions
chmod –reference=olleh hello

11.Create a script that adds execute permission to all subdirectories of the current directory for the owner, the group owner and all other users.
Regular files should not be changed.
 11-directories_permissions
chmod -R +111 */

12.Create a script that creates a directory called my_dir with permissions 751 in the working directory.
 12-directory_permissions
mkdir -m 751 my_dir

13.Write a script that changes the group owner to school for the file hello
 13-change_group
chgrp school hello

14.Write a script that changes the owner to vincent and the group owner to staff for all the files and directories in the working directory.
100-change_owner_and_group
chown vincent:staff *

15. Write a script that changes the owner and the group owner of _hello to vincent and staff respectively.
    • The file _hello is in the working directory
    • The file _hello is a symbolic link

101-symbolic_link_permissions
chown -h vincent:staff _hello

16. Write a script that changes the owner of the file hello to betty only if it is owned by the user guillaume.
102-if_only
chown --from=guillaume betty hello

17.Write a script that will play the StarWars IV episode in the terminal.
103-Star_Wars
telnet towel.blinkenlights.nl

