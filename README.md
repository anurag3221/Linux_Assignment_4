#Linux Assignment 4

# 1.Create a directory named "MyFiles" in your home directory. Navigate into this directory and list its contents.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ mkdir myfiles
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ ls
 Documents         Public
 Downloads        'Screenshot from 2024-02-05 11-43-12.png'
 htmlasssignment  'Screenshot from 2024-02-05 12-24-04.png'
 htmlCode         'Screenshot from 2024-02-05 12-39-00.png'
 index            'Screenshot from 2024-02-05 12-46-45.png'
 index1.html      'Screenshot from 2024-02-05 13-14-33.png'
 index.html        snap
 Music             Templates
 myfiles           Videos
 Pictures
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cd myfiles
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ touch s f h j
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ ls
f  h  j  s
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ 
```


# 2.Copy a file named "document.txt" from your home directory to the "MyFiles" directory. Move the file to a subdirectory named "Documents" within "MyFiles."
Ans- 
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ cd
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ touch document1.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ ls
 document1.txt     Pictures
 Documents         Public
 Downloads        'Screenshot from 2024-02-05 11-43-12.png'
 htmlasssignment  'Screenshot from 2024-02-05 12-24-04.png'
 htmlCode         'Screenshot from 2024-02-05 12-39-00.png'
 index            'Screenshot from 2024-02-05 12-46-45.png'
 index1.html      'Screenshot from 2024-02-05 13-14-33.png'
 index.html        snap
 Music             Templates
 myfiles           Videos
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cp document.txt myfiles
cp: cannot stat 'document.txt': No such file or directory
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cp document1.txt myfiles
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cd myfiles
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ ls
document1.txt  Documentss  f  h  j  s
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ cd
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cd myfiles
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ mv document.txt Documentss
mv: cannot stat 'document.txt': No such file or directory
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ mv document1.txt Documentss
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ ls
Documentss  f  h  j  s
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ cd Documentss
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Documentss$ ls
document1.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Documentss$ 
```


# 3.Create an empty file named "notes.txt" in the "MyFiles" directory. Afterward, delete the file.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cd myfiles
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ > notes.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ ls
Documentss  f  h  j  notes.txt  s
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ ls
Documentss  f  h  j  notes.txt  s
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ rm notes.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ ls
Documentss  f  h  j  s
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ 
```



# 4.Create a hard link named "hardlink.txt" for the file "document.txt" within the "Documents" subdirectory. Also, create a symbolic link named "symlink.txt" in the same location.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ cd Documentss
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Documentss$ ls
document1.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Documentss$ ln document1.txt hardlink1.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Documentss$ ls -lrth
total 0
-rw-rw-r-- 2 anurag anurag 0 Feb  5 15:37 hardlink1.txt
-rw-rw-r-- 2 anurag anurag 0 Feb  5 15:37 document1.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Documentss$ ln -s document.txt symlink.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Documentss$ ll
total 8
drwxrwxr-x 2 anurag anurag 4096 Feb  5 16:06 ./
drwxrwxr-x 3 anurag anurag 4096 Feb  5 15:42 ../
-rw-rw-r-- 2 anurag anurag    0 Feb  5 15:37 document1.txt
-rw-rw-r-- 2 anurag anurag    0 Feb  5 15:37 hardlink1.txt
lrwxrwxrwx 1 anurag anurag   12 Feb  5 16:06 symlink.txt -> document.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Documentss$ 
```



# 5.In the "MyFiles" directory, use a single command to list all files that start with the letter "a" and have a ".txt" extension.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cd myfiles
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ touch aa.txt aab.txt bcd.txt abc.txt dd.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ ls
aab.txt  aa.txt  abc.txt  bcd.txt  dd.txt  Documentss  f  h  j  s
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ cd
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ find ~/myfiles -type f -name 'a*.txt'
/home/anurag/myfiles/aab.txt
/home/anurag/myfiles/abc.txt
/home/anurag/myfiles/aa.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```


# 6.Rename all files in the "Documents" subdirectory of "MyFiles" with a ".bak" extension. Ensure the original file names are preserved.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cd myfiles
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ touch aa.txt aab.txt bcd.txt abc.txt dd.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ ls
aab.txt  aa.txt  abc.txt  bcd.txt  dd.txt  Documentss  f  h  j  s
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ cd
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ find ~/myfiles -type f -name 'a*.txt'
/home/anurag/myfiles/aab.txt
/home/anurag/myfiles/abc.txt
/home/anurag/myfiles/aa.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cd myfiles
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ ls
aab.txt  aa.txt  abc.txt  bcd.txt  dd.txt  Documentss  f  h  j  s
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ for file in *; do
>  mv "$file" "${file}.bak"
> done
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ ll
total 12
drwxrwxr-x  3 anurag anurag 4096 Feb  5 16:10 ./
drwxr-xr-x 23 anurag anurag 4096 Feb  5 15:36 ../
-rw-rw-r--  1 anurag anurag    0 Feb  5 16:08 aab.txt.bak
-rw-rw-r--  1 anurag anurag    0 Feb  5 16:08 aa.txt.bak
-rw-rw-r--  1 anurag anurag    0 Feb  5 16:08 abc.txt.bak
-rw-rw-r--  1 anurag anurag    0 Feb  5 16:08 bcd.txt.bak
-rw-rw-r--  1 anurag anurag    0 Feb  5 16:08 dd.txt.bak
drwxrwxr-x  2 anurag anurag 4096 Feb  5 16:06 Documentss.bak/
-rw-rw-r--  1 anurag anurag    0 Feb  5 15:34 f.bak
-rw-rw-r--  1 anurag anurag    0 Feb  5 15:34 h.bak
-rw-rw-r--  1 anurag anurag    0 Feb  5 15:34 j.bak
-rw-rw-r--  1 anurag anurag    0 Feb  5 15:34 s.bak
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ 
```


# 7.Use a wildcard character to copy all files from the "Documents" subdirectory of "MyFiles" to another directory named "Backup."
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ cd Documentss.bak
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Documentss.bak$ ls
document1.txt  hardlink1.txt  symlink.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Documentss.bak$ mkdir Backupp
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Documentss.bak$ cd
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ mkdir ~/myfiles/Backupp
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cp -r ~/myfiles/Documentss.bak/* ~/myfiles/Backupp/
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ ll
total 1220
drwxr-xr-x 23 anurag anurag   4096 Feb  5 15:36  ./
drwxr-xr-x  5 root   root     4096 Feb  5 11:47  ../
-rw-------  1 anurag anurag  12288 Jan 15 12:19  .anurag.swp
-rw-------  1 anurag anurag   8002 Feb  5 15:26  .bash_history
-rw-r--r--  1 anurag anurag    220 Jan  8 18:44  .bash_logout
-rw-r--r--  1 anurag anurag   3771 Jan  8 18:44  .bashrc
drwxr-xr-x 18 anurag anurag   4096 Jan 19 00:37  .cache/
drwx------ 20 anurag anurag   4096 Jan 31 00:43  .config/
-rw-rw-r--  1 anurag anurag      0 Feb  5 15:36  document1.txt
drwxr-xr-x  2 anurag anurag   4096 Feb  5 15:24  Documents/
drwxrwxr-x  3 anurag anurag   4096 Jan 24 00:35  .dotnet/
drwxr-xr-x  2 anurag anurag   4096 Feb  5 11:24  Downloads/
drwx------  3 anurag anurag   4096 Feb  5 10:41  .gnupg/
-rw-rw-r--  1 anurag anurag    120 Jan 18 15:23  htmlasssignment
drwxrwxr-x  2 anurag anurag   4096 Jan 19 10:33  htmlCode/
-rw-rw-r--  1 anurag anurag    120 Jan 18 12:29  index
-rw-rw-r--  1 anurag anurag      0 Jan 24 00:17  index1.html
-rw-rw-r--  1 anurag anurag    151 Jan 18 15:22  index.html
drwxr-xr-x  3 anurag anurag   4096 Jan  9 00:50  .local/
drwx------  4 anurag anurag   4096 Jan  9 00:58  .mozilla/
drwxr-xr-x  2 anurag anurag   4096 Jan  9 00:50  Music/
drwxrwxr-x  4 anurag anurag   4096 Feb  5 16:12  myfiles/
drwxr-xr-x  2 anurag anurag   4096 Feb  5 13:14  Pictures/
drwx------  3 anurag anurag   4096 Jan  9 15:15  .pki/
-rw-r--r--  1 anurag anurag    807 Jan  8 18:44  .profile
drwxr-xr-x  2 anurag anurag   4096 Jan 10 21:37  Public/
drwxrwxr-x  4 anurag anurag   4096 Jan 30 10:23  .qet/
-rw-rw-r--  1 anurag anurag 146570 Feb  5 11:44 'Screenshot from 2024-02-05 11-43-12.png'
-rw-rw-r--  1 anurag anurag 236722 Feb  5 12:27 'Screenshot from 2024-02-05 12-24-04.png'
-rw-rw-r--  1 anurag anurag 152524 Feb  5 12:39 'Screenshot from 2024-02-05 12-39-00.png'
-rw-rw-r--  1 anurag anurag 253116 Feb  5 12:47 'Screenshot from 2024-02-05 12-46-45.png'
-rw-rw-r--  1 anurag anurag 307109 Feb  5 13:14 'Screenshot from 2024-02-05 13-14-33.png'
drwx------  5 anurag anurag   4096 Jan 19 10:27  snap/
drwx------  2 anurag anurag   4096 Jan  9 00:52  .ssh/
-rw-r--r--  1 anurag anurag      0 Jan  9 14:44  .sudo_as_admin_successful
drwxr-xr-x  2 anurag anurag   4096 Jan  9 00:50  Templates/
drwx------  6 anurag anurag   4096 Jan  8 15:03  .thunderbird/
drwxr-xr-x  2 anurag anurag   4096 Jan  9 00:50  Videos/
-rw-------  1 anurag anurag   6912 Jan 19 14:51  .viminfo
drwxrwxr-x  4 anurag anurag   4096 Jan 19 10:31  .vscode/
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cd myfiles
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles$ cd  Backupp
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Backupp$ ll
total 12
drwxrwxr-x 3 anurag anurag 4096 Feb  5 16:13 ./
drwxrwxr-x 4 anurag anurag 4096 Feb  5 16:12 ../
drwxrwxr-x 2 anurag anurag 4096 Feb  5 16:13 Backupp/
-rw-rw-r-- 1 anurag anurag    0 Feb  5 16:13 document1.txt
-rw-rw-r-- 1 anurag anurag    0 Feb  5 16:13 hardlink1.txt
lrwxrwxrwx 1 anurag anurag   12 Feb  5 16:13 symlink.txt -> document.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~/myfiles/Backupp$ 
```



# 8.Execute the ls command to list files in the current directory. Save the output to a file named "file_list.txt." Then, use a pipe to filter the output through grep to display only files with a ".txt" extension.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ ls >file_list.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ ls
 document1.txt   file_list.txt     index         Music      Public                                    'Screenshot from 2024-02-05 12-39-00.png'   snap
 Documents       htmlasssignment   index1.html   myfiles   'Screenshot from 2024-02-05 11-43-12.png'  'Screenshot from 2024-02-05 12-46-45.png'   Templates
 Downloads       htmlCode          index.html    Pictures  'Screenshot from 2024-02-05 12-24-04.png'  'Screenshot from 2024-02-05 13-14-33.png'   Videos
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ ls >file_list.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ grep '\.txt$' file_list.txt
document1.txt
file_list.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```



# 9.Create a new text file named "my_notes.txt" using the touch command. Open the file in the Vim editor, add some text, and save the changes.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ touch my_notes.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ vim my_notes.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```


# 10.Run the date command and store the output in a variable named "current_date." Display the value of the variable and append it to the "my_notes.txt" file.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ current_date=$(date)
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ echo "Current Date: $current_date"
Current Date: Monday 05 February 2024 04:19:08 PM IST
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ echo "Current Date: $current_date" >> my_notes.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cat my_notes.txt
I love lucky
Mai mar jayunga
Current Date: Monday 05 February 2024 04:19:08 PM IST
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```



# 11.Edit the Bash startup script (e.g., .bashrc) to set an environment variable named "CUSTOM_PATH" to a specific directory path. Ensure the variable is available in new shell sessions.
Ans-



# 12.Use the echo command to add a new line of text to the "my_notes.txt" file without overwriting existing content. Verify that the new text is appended.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cat my_notes.txt
I love lucky
Mai mar jayunga
Current Date: Monday 05 February 2024 04:19:08 PM IST
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ echo "lucky lover" >>my_notes.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cat my_notes.txt
I love lucky
Mai mar jayunga
Current Date: Monday 05 February 2024 04:19:08 PM IST
lucky lover
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```

# 13.List all files in the "/etc" directory, filter the output to include only those containing the word "conf," and save the result to a file named "conf_files.txt."
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo find /etc -type f -name "*conf*" > conf_files.txt
[sudo] password for anurag: 
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ cat conf_files.txt
/etc/environment.d/90atk-adaptor.conf
/etc/environment.d/90qt-a11y.conf
/etc/speech-dispatcher/modules/kali.conf
/etc/speech-dispatcher/modules/epos-generic.conf
/etc/speech-dispatcher/modules/dtk-generic.conf
/etc/speech-dispatcher/modules/ivona.conf
/etc/speech-dispatcher/modules/swift-generic.conf
/etc/speech-dispatcher/modules/espeak-mbrola-generic.conf
/etc/speech-dispatcher/modules/baratinoo.conf
/etc/speech-dispatcher/modules/espeak-generic.conf
/etc/speech-dispatcher/modules/espeak-ng.conf
/etc/speech-dispatcher/modules/festival.conf
/etc/speech-dispatcher/modules/llia_phon-generic.conf
/etc/speech-dispatcher/modules/mary-generic.conf
/etc/speech-dispatcher/modules/espeak.conf
/etc/speech-dispatcher/modules/cicero.conf
/etc/speech-dispatcher/modules/pico-generic.conf
/etc/speech-dispatcher/modules/espeak-ng-mbrola-generic.conf
/etc/speech-dispatcher/modules/ibmtts.conf
/etc/speech-dispatcher/modules/flite.conf
/etc/speech-dispatcher/speechd.conf
/etc/speech-dispatcher/clients/emacs.conf
/etc/apport/crashdb.conf
/etc/fonts/conf.d/65-khmer.conf
/etc/fonts/fonts.conf
/etc/fonts/conf.avail/20-unhint-small-dejavu-lgc-sans.conf
/etc/fonts/conf.avail/65-0-fonts-gujr-extra.conf
/etc/fonts/conf.avail/67-smc-uroob.conf
/etc/fonts/conf.avail/58-dejavu-lgc-sans-mono.conf
/etc/fonts/conf.avail/65-khmer.conf
/etc/fonts/conf.avail/66-lohit-telugu.conf
/etc/fonts/conf.avail/65-fonts-persian.conf
/etc/fonts/conf.avail/99-language-selector-zh.conf
/etc/fonts/conf.avail/10-hinting-slight.conf
/etc/fonts/conf.avail/67-smc-suruma.conf
/etc/fonts/conf.avail/59-lohit-devanagari.conf
/etc/fonts/conf.avail/58-dejavu-lgc-serif.conf
/etc/fonts/conf.avail/10-sub-pixel-bgr.conf
/etc/fonts/conf.avail/25-unhint-nonlatin.conf
/etc/fonts/conf.avail/67-smc-keraleeyam.conf
/etc/fonts/conf.avail/67-smc-chilanka.conf
/etc/fonts/conf.avail/57-dejavu-serif.conf
/etc/fonts/conf.avail/10-no-sub-pixel.conf
/etc/fonts/conf.avail/80-delicious.conf
/etc/fonts/conf.avail/67-smc-anjalioldlipi.conf
/etc/fonts/conf.avail/30-metric-aliases.conf
```


# 14.Open the "my_notes.txt" file in Vim. Use Vim's search and replace functionality to replace all occurrences of the word "important" with "critical." Save the changes.
Ans-
```
![alt text](file:///home/anurag/Pictures/Screenshot%20from%202024-02-05%2016-28-13.png)

anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ vim my_notes.txt
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```


# 15.Create a new user account named "john_doe." Set the user's home directory to "/home/john_doe" and assign the user to the "users" group.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo adduser --home /home/john_doee --ingroup users john_doee
Adding user `john_doee' ...
Adding new user `john_doee' (1002) with group `users' ...
Creating home directory `/home/john_doee' ...
Copying files from `/etc/skel' ...
New password: 
Retype new password: 
passwd: password updated successfully
Changing the user information for john_doee
Enter the new value, or press ENTER for the default
	Full Name []: 
	Room Number []: 
	Work Phone []: 
	Home Phone []: 
	Other []: 
Is the information correct? [Y/n] 
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ id john_doee
uid=1002(john_doee) gid=100(users) groups=100(users)
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```


# 16.Add the user "john_doe" to the sudoers file, allowing them superuser privileges. Confirm that "john_doe" can execute commands with sudo.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo visudo
[sudo] password for anurag: 
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo ls /root
snap
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```


# 17.Modify the user account "john_doe" to change the default shell to "/bin/bash" and set the account's expiration date to one month from today.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo chsh -s /bin/bash john_doee
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo chage -E $(date -d "+1 month" +"%Y-%m-%d") john_doee
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo chage -E $(date -d "2022-03-15 month" +"%Y-%m-%d") john_doee
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ getent passwd john_doee
john_doee:x:1002:100:,,,:/home/john_doee:/bin/bash
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo chage -l john_doee
Last password change					: Feb 05, 2024
Password expires					: never
Password inactive					: never
Account expires						: Apr 15, 2022
Minimum number of days between password change		: 0
Maximum number of days between password change		: 99999
Number of days of warning before password expires	: 7
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```


# 18.Create a new group named "development_team." Add "john_doe" to this group and verify the group's existence.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo groupadd development_team
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo usermod -aG development_team john_doee
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ grep development_team /etc/group
development_team:x:1002:john_doee
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ getent group development_team
development_team:x:1002:john_doee
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```


# 19.Remove "john_doe" from the "users" group and add them to the "development_team" group. Confirm the changes.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo deluser john_doee users
/usr/sbin/deluser: You may not remove the user from their primary group.
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo usermod -aG development_team john_doee
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ id john_doee
uid=1002(john_doee) gid=100(users) groups=100(users),1002(development_team)
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```

# 20.Delete the user account "john_doe" and ensure that their home directory is also removed.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo userdel -r john_doee
userdel: user 'john_doee' does not exist
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```

# 21.Delete the group "development_team" and ensure that all users previously belonging to the group are appropriately handled.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo groupdel development_team
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```

# 22.Implement a password policy that requires users to change their passwords every 90 days. Apply this policy to all existing and new user accounts.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo chage -M 98 -I -1 -E -1 sumit
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```


# 23.Manually lock the user account "john_doe." Attempt to log in as "john_doe" to confirm that the account is locked. Then, unlock the account.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo passwd -l sumit
passwd: password expiry information changed.
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ su - sumit
Password: 
su: Authentication failure
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo passwd -u sumit
passwd: password expiry information changed.
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```


# 24.Use the id command to display detailed information about the "john_doe" user, including user ID, group ID, and supplementary groups.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ id sumit
uid=1001(sumit) gid=1001(sumit) groups=1001(sumit)
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```

# 25.Configure the password aging for the user "john_doe" to enforce a maximum password age of 60 days. Confirm that the changes take effect.
Ans-
```
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo chage -l sumit
Last password change					: Jan 09, 2024
Password expires					: Apr 16, 2024
Password inactive					: never
Account expires						: never
Minimum number of days between password change		: 0
Maximum number of days between password change		: 98
Number of days of warning before password expires	: 7
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ sudo chage -M 60 sumit
anurag@anurag-Lenovo-IdeaPad-S145-15IKB:~$ 
```



