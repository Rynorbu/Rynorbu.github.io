---
Title: SWS101 Linux Command
categories: [SWS101, Linux commands]
tags: [SWS101]
---
## Topic: Linux Commands
---

In class, we played a bandit wargame which teaches the basic linux commands. Inorder to go to the next level, our goal is to find the password hidden in each levels.

#### Level 0

In this task, the aim is to log in to SSH. To do that, we need three things: a username, an IP address, and a port number. To connect, we have to use the host "bandit.labs.overthewire.org" on port 2220. The username is "bandit0," and the password is also "bandit0."

The command to get into SSH is

`ssh bandit0@bandit.labs.overthewire.org -p 2220`

* SSH: Stands for 'Secure Shell'. It's a secure way to connect to and communicate with another computer over the internet.

---
#### level 0-1

In this level, our goal is to discover the password for the next level, and it's hidden in a file called "readme" within the home directory. I tried the "cat" command, and it worked. This command helps concatenates files and also display what's inside them.

---
#### level 1-2

To get the password for the next level, it's in the home directory. However, using the "cat" command directly won't work because it thinks "-" is a flag. To fix this, I used "./" to tell the computer to look in the current directory.

#### level 2-3

The password is stored in a file named "spaces" in the home directory.  I tried using the "cat" command with the filename "spaces in this filename"  but an error occured because it doesn't recognize that "spaces in this filename" is a single argument. To solve this, I used quotation marks and also put a backslash before each space.

---
#### level 3-4

To find the password in this level, it's stored in a hidden file within the "inhere" directory. I used the "cd" command to go into that directory and the "cat" command to read the hidden file.
* cd: Stands for change directory. It helps to navigate to different folder.
 
---
#### level 4-5
The password for the next level is stored in the only human-readable file in the inhere directory. In this level, I learned to go loop through each file and check if it's a human readable file. By doing this, I discovered that file 7 is readable and has the password stored inside.

---
### level 5-6

I found the password using the "find" command. Because the password is in a file that's human readable, exactly 1033 bytes, and not an executable, I used the "find -type f -size 1033c !-executable" command. This helped me locate the password in the "file2."

* find = This command helps to find and display the paths of files with the specified name in the specified directory

---
### level 6-7

To find the password in this level, I used the "find" command. Since the password is somewhere on the server in the directory, owned by user bandit7, group bandit6, and 33 bytes in size, I ran the command "find / -user bandit7 -group bandit6 -size 33c." This helped me discover that the password is in the file "/var/lib/dpkg/info/bandit7.password."

---
### level 7-8

The password for the next level is in a file called data.txt, right next to the word "millionth." Since there are many files in data.txt, it's tough to search them one by one. So, I used the "grep" command, which helps search for specific text in files.

* grep: Stands for "global regular expression print." It is used for searching and filtering text data in files. And the symbol "|" is used to filter out useless information.

---
### level 8-9

The password for the next level is in data.txt. Since there are many lines in the file, the password is the one that appears only once. I sorted the lines in ascending order, counted how many times each line appears, and found the line that appears only once.

* sort: used to print the output of a file in given order. 
* uniq -c:  helps to filter out repeated lines in a file.

---
### level 9-10

To find the password in data.txt where the password is a human-readable string with several '=' characters, I used the strings command to extract readable strings from the file and then used grep to search for text containing '='. This approach helped me to  locate the unique string that serves as the password.

* string: used to extract readable strings from a file. 
* grep: It searches for text and strings defined by users in a given file.

---
### level 10-11

The password is in data.txt, which has base64 encoded data. Base64 is a way to convert binary data into text. Since the password is encoded, we can decode it using the -d option with the base64 command.

* Linux has a command called base64 that allows for encoding and decoding in Base64. For decoding, we need to use the flag -d.

---
### level 11-12

I used the tr command and rot13 to find the password in data.txt. This is because all lowercase and uppercase letters have been rotated 13 positions, and I needed to translate and replace each letter 13 times to get the password.

* tr: translates or deletes characters from standard inputand writes the result to standard output.
* rot13: It replaces a letter with the letter 13 letters after it in the alphabet.

---
### level 12-13

The password for the next level is stored in the file data.txt, which is a hexdump of a file that has been repeatedly compressed. In this level I have studied about the commands that can make, copy and move files. I have learned to how to decompress the given file until it is in normal file.

* mkdir: can be used to create a new directory.
* cp: used to copy files.
* mv: moves or renames files.
* gzip: used to compress files, effectively reducing their size.
* tar: used to create archive and extract the Archive files.

---
### level 13-14

In this level, we are not provided with a password to access bandit14.  We are, however, provided with the private ssh key which can be used to log into the next level.
In this level I have learned to navigate to various servers using SSH protocol – to login without a password. I connected to the localhost using the ssh command and used the -i option to specify the sshkey.private file.

* -i: It's an option in the SSH command that lets you specify the private key file you want to use to login.

---
### level 14-15

The password for the next level can be retrieved by submitting the password of the current level to port 30000 on localhost. We need to submit the password to port 30000 on localhost. I used nc to connect to localhost port 3000 and write the password.

* nc or netcat is a command that allows to read and write data over a network connection. It can be used for TCP and UDP connections.

---
### level 15-16

Since the task states that the password can be retrieved using SSL encryption, I connect to the localhost server with the OpenSSL client and send the password from this level. The server then sends back the password for the next level.

* OpenSSL is a library for secure communication over networks.

* Openssl s_client is the implementation of a simple client that connects to a server.

---
### level 16-17

I used the service discovery from nmap and noticed that there were 5 open ports. I used OpenSSL again to connect to the specified port on localhost and sent the password.

* nmap is a network scanner.
* -p this flag lets us choose which ports to scan.
* The -sV flag lets us do a service/version detection scan.


---
### level 17-18

The password for the next level is in passwords.new and is the only line that has been changed between passwords.old and passwords.new. I used "diff" command to find the password. 

* diff command prints the difference between two files.

---
### level 18-19

The password was stored in the readme file in the home directory. Due to the modification of the '.bashrc' file, using the 'cat' command to access the file is not possible. Instead, I used the SSH command with the '-t' option to find the password, as it instructs the computer to act as its real terminal.

* .bashrc is a file that runs every time a terminal is loaded, and this includes instances of logging in through SSH since it also loads a terminal.

---
### level 19-20

We can't read file that we don't have permission to read, but this program let us do that. In this level by using a, “./bandit20-do”, it allows running commands as if I were another user. The permissions and owners of a file can be seen using the ls -l command. 

* Suid is a special permission.



