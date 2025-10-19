# Week 3.1 File management

## File management
1.   Create a new directory in the homedirectory called Documents
#
    root@7a3c2be130d1:/home/ubuntu# mkdir documents
    root@7a3c2be130d1:/home/ubuntu# ls
    documents

2.  Create in that folder a new empty file called file1. *Note: use touch*
#
    root@7a3c2be130d1:/home/ubuntu/documents# touch file1
    root@7a3c2be130d1:/home/ubuntu/documents# ls
    file1

3.  Copy file1 to the root of the homedirectory, use the shortest command
#   
    root@7a3c2be130d1:/home/ubuntu/documents# cp file1 ../
    root@7a3c2be130d1:/home/ubuntu/documents# cd ..
    root@7a3c2be130d1:/home/ubuntu# ls
    documents  file1

4.  Create with 1 command 8 empty files in the directory Documents with the names, file2, file3, ..., file20. Use the shortest command.
#
    root@7a3c2be130d1:/home/ubuntu# touch documents/file{2..9}
    root@7a3c2be130d1:/home/ubuntu# cd documents
    root@7a3c2be130d1:/home/ubuntu/documents# ls
    file1  file2  file3  file4  file5  file6  file7  file8  file9
    root@7a3c2be130d1:/home/ubuntu/documents#

5. Create a new directory called backup in the homedirectory
#   
    root@7a3c2be130d1:/home/ubuntu# mkdir backup
    root@7a3c2be130d1:/home/ubuntu# ls
    backup  documents  file1
    root@7a3c2be130d1:/home/ubuntu#

6. Copy only the even files from Documents to Backup
#
    root@7a3c2be130d1:/home/ubuntu# cp documents/file[02468]* backup
    root@7a3c2be130d1:/home/ubuntu# ls
    backup  documents  file1
    root@7a3c2be130d1:/home/ubuntu# cd backup
    root@7a3c2be130d1:/home/ubuntu/backup# ls
    file2  file4  file6  file8
    root@7a3c2be130d1:/home/ubuntu/backup#

7. Create a hidden file in the homedirectory
#
    root@7a3c2be130d1:/home/ubuntu# touch .hiddenfile
    root@7a3c2be130d1:/home/ubuntu# ls -a
    .  ..  .bash_logout  .bashrc  .hiddenfile  .profile  backup  documents  file1
    
8. Show all hidden files
#
    root@7a3c2be130d1:/home/ubuntu# ls -a
    .  ..  .bash_logout  .bashrc  .hiddenfile  .profile  backup  documents  file1

9. Create a new directory in the homefolder with the name *Subdir*
#
    root@7a3c2be130d1:/home/ubuntu# mkdir Subdir
    root@7a3c2be130d1:/home/ubuntu# ls
    Subdir  backup  documents  file1

10. Move and rename the file file2 (from q2) to this folder with the name *TextfileQ8*
#
    root@7a3c2be130d1:/home/ubuntu# mv documents/file2 Subdir/textfileQ8
    root@7a3c2be130d1:/home/ubuntu# cd Subdir
    root@7a3c2be130d1:/home/ubuntu/Subdir# ls
    textfileQ8


11. Show in the long listing format the full content (also hidden files and directories) of the homedirectory with all subdirectories and the subdirectories of that, ...
#
    root@7a3c2be130d1:/home/ubuntu# ls -laR
    .:
    total 36
    drwxr-x--- 1 ubuntu ubuntu 4096 Oct 13 14:33 .
    drwxr-xr-x 1 root   root   4096 Oct  6 15:14 ..

12. Delete the directory *Subdir* with all content.
#
    root@7a3c2be130d1:/home/ubuntu# rm -rf Subdir
    root@7a3c2be130d1:/home/ubuntu# ls
    backup  documents  file1

13. Show only the owner of the file *words*
#
    root@7a3c2be130d1:/home# stat -c "%U" words
    root

## Case John
John is working on a big project in Linux that has several configuration files. Help him to copy the following files to a new folder in the homedrive called backup_config.
- /etc/hosts
- ~/.bashrc
- /etc/passwd
- /etc/shadow
#
    root@7a3c2be130d1:/home/ubuntu# cd backup_config
    root@7a3c2be130d1:/home/ubuntu# cp /etc/hosts ~/.bashrc /etc/passwd /etc/shadow /home/ubuntu/backup_config
    root@7a3c2be130d1:/home/ubuntu/backup_config# ls -a
    .  ..  .bashrc  hosts  passwd  shadow

Then create a file with the directory listing of the files in that folder. *Note: show the long listing format, with hidden files and in human readable.*
#
    root@7a3c2be130d1:/home/ubuntu# ls -lha > directory_listing.txt
    root@7a3c2be130d1:/home/ubuntu# ls
    backup  backup_config  directory_listing.txt  documents  file1

## Case Jean
Jean has some photo's he would like to rename, how ever since that didn't work out very well on PowerShell he asks to provide a testcase with 1 blank files in Linux. Rename the file  to the inode number of that file. To help you John has already written the command to read out a command in a variable. 
- Step 1: Get the inode command
- Step 2: Insert that command in a variable called inode: `inode=$(INSERT_COMMAND_STEP1)`
- Step 3: Use `echo $inode` to check if it works
- Step 4: Rename the file
#
    root@7a3c2be130d1:/home/ubuntu# touch photo1
    root@7a3c2be130d1:/home/ubuntu# ls
    backup  backup_config  directory_listing.txt  documents  file1  photo1
    root@7a3c2be130d1:/home/ubuntu# ls -i photo1
    309479 photo1
    root@7a3c2be130d1:/home/ubuntu# inode=$(ls -i photo1 | awk '{print $1}')
    root@7a3c2be130d1:/home/ubuntu# echo $inode
    309479
    root@7a3c2be130d1:/home/ubuntu# mv photo1 $inode
    root@7a3c2be130d1:/home/ubuntu# ls
    309479  backup  backup_config  directory_listing.txt  documents  file1

The result should be for example: 21374992

## Case Sophie
Sophie thinks Douglas has hidden something on the system. Show all hidden files with an x or i in the name in the folder /sys/module.
# 
    find /sys/module -type f -name ".*[xi]*"
*Note: use find and show the output via ls*
#
    ls -l $(find /sys/module -type f -name ".*[xi]*" 2>/dev/null)

Create manual softlinks to those files in the homedirectory to easily get back to them.


## Case LEHO quiz - evaluation
Answer the found keys in the LEHO quiz

Run the following docker container: `docker run -it --name caoslab3 koenkoreman/caos_lab3 /bin/bash`
If the container has run before use `docker start -i caoslab3` to start the container.

1. Create a new directory called *linuxfiles* in the directory `/home`. 
2. Create a file called config.yml in the linuxfiles folder with the following contents:

```yml
### Config file for the lab FileManagement by KoenK
### Do not change this file
name: Koen K

lessons:
  - Virtualizationcd
  - Linux Commands
  - Docker

contact:
  koen.koreman@howest.be
```
3. Copy file /etc/mysetup.conf to the linuxfiles folder
4. Create a hidden file with the name secret in the folder linuxfiles
5. Create a softlink to the `/etc/passwd` file in the folder linuxfiles

Execute the command `val` to retrieve the keys

Q1 - autochecking
## CORRECT - KEY ## - a467c744
Q2 - autochecking
Q3 - autochecking
## CORRECT - KEY ## - 149d2a6f
Q4 - autochecking
## CORRECT - KEY ## - 2dd66a1
Q5 - autochecking
## CORRECT - KEY ## - af2c56me
root@0f53ceb90a26:/home/linuxfiles# 