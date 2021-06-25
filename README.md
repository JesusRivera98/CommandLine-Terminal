# CommandLine-Terminal
This repo is from Platzi's course "Introducción a la Terminal y Línea de Comandos"

## Route Descriptors
| Command | Description |
| --------- | --------- |
|/ | System root path|
|. | Current directory|
|.. | Previous Directory|
|~ | User's home directory |

## Keyboard shortcuts:

| Command | Description |
| --------- | --------- |
|CTRL-C | Terminates the process of a command in the terminal|
|CTRL-D | Terminates the input of a command|
|CTRL-A | Advances to start of line|
|CTRL-E | Advances to end of line|
|CTRL-L | Clears the terminal screen|

## Directory operations:

| Command | Description |
| --------- | --------- |
|pwd | Print current directory|
|mkdir dir1 | Create the directory named dir1|
|cd dir1 | Changes to the directory named dir1|
|cd ../ .. | Change two previous directories from the current one|
|cd | Change to the user's home directory|
|ls | Show files and directories|
|tree / path | Shows all files and directories nested within the path to any depth level|
|tree -L 2. | Show all files and directories nested within|


## ls operations:

| Command | Description |
| --------- | --------- |
|-a | Show everything (including hidden files)|
|-R | Display a list recursively|
|-r | Show reverse listing|
|-t | Show last modified|
|-S | Sample sorting by size|
|-l | Display using long format|

## File and directory manipulation:

| Command | Description |
| --------- | --------- |
|touch newFile | Create a new file called newFile
|file my_file | Shows the characteristics of my_file
|cp file1 / destination | Copy the file file1 to the path / destination
|cp -r dir1 dir1_cp | Copy directory dir1 and its contents to a new one called dir1_cp
|mv file1 / destination | Move file file1 to path / destination
|mv file1 ok_file | Rename the file file1 to the name ok_file
|rm file1 | Delete file file1
|rm -ri dir1 | Remove directory dir1 and its contents interactively
|rm -r dir1 | Remove directory dir1 and its contents In a direct way
|ln -s file link_name | Creates a symbolic link to the file 
|open filename | Open the file with the program default (macOS)
|xdg-open filename | Open the file with the program default (most Linux systems)

## Handling text files:

| Command | Description |
| --------- | --------- |
|head file.txt | Displays the first 10 lines of text from the file file.txt |
|head -n 20 file.txt | Displays the first 20 lines of text from the file file.txt|
|tail file.txt | Displays the last 10 lines of text from the file file.txt|
|tail -n 20 file.txt | Displays the last 20 lines of text from the file file.txt|
|less file.txt | Explore the file content with pagination|
|cat file1 file2 | Concatenates the contents of file1 and file2 to the terminal exit|

## Command exploration and help within the terminal:

| Command | Description |
| --------- | --------- |
|man command | Displays the user manual of the command|
|help command | Displays help for the command (only it works if the shell is Bash)|
|which command | Displays the path of where it is located the command executable|
|whatis command | Briefly shows the function of the command|
|alias aliasname = ”command” | Create an alias for the command|
|alias l = ”ls -la” | Create an alias for the ls command with options called l|

## Wildcards:

| Command | Description |
| --------- | --------- |
|* | Matches any character|
|? | Matches any single character|
|[characters] | Matches any character that is a member from the character set|
|[! characters] | Matches any character other than character set member|
|[[: class:]] | Matches any character in the class|

## Classes within the Wildcards:

| Command | Description |
| --------- | --------- |
|[: alnum:] |Matches any alphanumeric character|
|[: alpha:] |Matches any alphabetic character|
|[: digit:] |Matches any number|
|[: lower:] |Matches any lowercase letter|
|[: upper:] |Matches any uppercase letter|

## I / O redirects and control operators:

| Command | Description |
| --------- | --------- |
|command <file | Redirects the input of a command to a file
|command> file | Redirects the output of a command to a file (use with care because overwrites the |system)|
|command >> file | Concatenates the output of a command to a file. If it doesn't exist, create it.
|command 2> error.txt | Redirect the error output of a command to the error.txt file
|command1 | command2 | Redirects the output of command1 to the command2 input
|command1; command2 | Run consecutively
|command1 & command2 | Run asynchronously
|command1 && command2 | Executes command2 if and only if the command1 was executed successfully|
|command1 \|\| command2 | Run command1 or command2|


## Management of permissions and users:
### Mode type:

| Owner | Group | World |
| --------- | --------- | --------- |
| rwx | r-x | r-x |
| 1 1 1 | 1 0 1 | 1 0 1 |


### Octal mode:

| Octal | Binary | Permissions |
| --------- | --------- | --------- |
|0 | 000 | --- |
|1 | 001 | --x |
|2 | 010 | -w- |
|3 | 011 | -wx |
|4 | 100 | r-- | 
|5 | 101 | r-x | 
|6 | 110 | rw- |
|7 | 111 | rwx |

### Symbolic mode:

| Symbol | Meaning |
| --------- | --------- |
|u | Only for the user|
|g | Only for the group|
|o | Only for others (it's the world)|
|a | Applies to everyone |


## 

| Command | Description |
| --------- | --------- |
|chmod 755 mytext | Change the file permissions to 755
|chmod u-r mytext | Remove read permission to file
|chmod u = rwx, go = r mytext | Add read, write, and run to user and read only the group and others.
|id | Displays the user ID
|whoami | Shows the name of the logged in user
|your username | Change user
|sudo command | Run a command as superuser


## Environment Variables:

| Command | Description |
| --------- | --------- |
|env | Print current environment variables|
|echo $VAR | Print the environment variable VAR|
|$PATH | Variable where the executable paths are|
|$HOME | User's home directory|
|export $VAR = val | Assigns the variable $ VAR with the value val|

## Search commands:

| Command | Description |
| --------- | --------- |
|find <path> -name <name> | Search in a path and with a file name|
|find. -name agenda | Find the file with the name agenda in the current directory|
|grep <regex> file | Search with regular expressions within a file or terminal output|
|grep -i hello message.txt | Search for the word hello ignoring lowercase and uppercase|


## Network utilities:

| Command | Description |
| --------- | --------- |
|ifconfig | Show network information|
|ping ip_domain | Check the availability of the resource|
|curl ip_domain | Query a resource either by IP address or by domain and show it in terminal|
|wget ip_domain | Download a resource either by IP address or by domain|
|traceroute ip_domain | Shows the packet path to an IP or domain|
|netstat -i | Show network interfaces and their status|
  
## Compress files:
tar -czvf <name> .tar.gz <directory_name>
### Example:
tar -czvf my_files.tar.gz Documents
## Unzip files:
tar -xzvf <name> .tar.gz <directory_name>
### Example:
tar -xzvf my_files.tar.gz Documents
