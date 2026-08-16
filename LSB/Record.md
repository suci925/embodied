# Linux Command learning record 
## 2026-8-7
### file and directory operations
| Command | Example | Function | My Understanding |
|---------|---------|----------|------------------|
| pwd     | pwd     | print the work catalogue| print the current directory path |
| cd | cd [DIRECTORY] |change directory | The path used to specify the location of my work |
| cd . | cd . | Represent the directory you are currently in| The path remains unchanged |
| cd .. | cd .. | Move you up one level to the one that contains the current directory | Return to the previous level |
| cd ~ | cd ~ | A shortcut to your personal family directorty | Return directly to the root directory |
| ls | ls | List the files and directories | List the subdirectories under the current file |
| ls -a | ls -a | View hidden files | View all files |
| ls -l | ls -l | Get detailed information | Display specific information |
| ls -lh | ls -lh | Human-readable output | Simplify the file size for essier understanding | 
| ls -r | ls -r | OrderByDescending | List the files and directories in reverse order |
| ls -lt | ls -lt | sort by modification time | ls -ltr: Sort by modification time and then reverse sort |
| ls  -lS | ls -lS | Sort by file size | | |
| ls -ld | ls -ld | List the directory itself,  not its contents | |
| touch | touch | Create new document | The main purpose is to change the file timestamp, but it is also often used to create new empty files. |
| ls -l [directory] | check the timestamp |  |  |
| touch -r file1.txt file2.txt | Copy the timestamp from one file to another |  |  |
| touch -d "2026-08-07 13:04:45" myfile | set a specific date and time |  |  |
| touch -c myfile.txt | Update the existing files |  |  |
| touch -a myfile.txt | Only change the access time |  |  |
| touch -m myfile.txt | Only change the modification time |  |  |
| touch -c myfile.txt | If the file does not exist, please do not create it. |  |  |
| touch -t stamp | Use timestamps in a concise numerical format |  |  |
### The problem I encountered today
1. Why do some file names start with a dot?
A1: The click is hidden by default and usually stores the configuration.
2. Why do I only list the directory itself?
A2: Use ls -d directory/.
### It will be verified next week

## 2026-8-10
### file and cat 
| command | function | My understanding |
|---------|----------|------------------|
| file [directory] | To know what type the file is | Display the description of the file content |
| display mime type |                                 |  |
|-------------------|---------------------------------|--|
| file -i [directory] | Display MIME type information |  |
| file -b [directory] | in short mode, the file name is omitted in the output. |  |
| file -L [directory] | Please follow the symbolic link. |  |
| file -z [directory] | Try to check the compressed file. |  |
| cat |                                                                   |  |
|-----|-------------------------------------------------------------------|--|
| cat [directory] | Display the content of a single file in the terminal. |  |
| cat file1.txt file2.txt | Merge or concatenate multiple files and display their merged output. It reads files in the provided order and prints them in sequence. | Merge or concatente multiple files and display their merged output  |
| cat file2.txt file2.txt > file3.txt | Save the merged output to a new file |  |
| cat > file.txt | Create a file with redirection | Create a new file or overwrite the original file and edit its content. |
| cat >> file.txt | Attach files rather than overwrite. | edit the file |
| cat -n file.txt | Number all output lines, starting from 1.|  |
| cat -b file.txt | Only number non-empty output lines |  |
| cat -s file.txt | Compress multiple blank into one. |  |
| cat -A file.txt |  Display non-print characters,tabs and line endings. |  |
### The problem I encountered today:
A1: What's the difference between > and >> ?
Q: > overwrite file,>> Attached at the end of the file/.
| Less |             |                 |
|------|-------------|-----------------|
| Command | function | Myunderstanding |
| less file.txt | Display text in a paginated format , allowing you to browse files without overwhelming the termial. |  |
| Navigation and Control |
|------------------------|
| Arrow keys and page keys : Use 'Page up' 'Page down' ' up ' 'down' , navigate line by line or page by page. |
| Enter the starting: press the key 'g' directly to move to the beginning of the text file. |
| Enter the end: press 'shift+g' to jump to the end of the text file. |
| Move half a page :press the key 'u' 'd' to moveup or down. |
| Help menu : If you forget a command indide less, simply click to 'h' display a useful summary. |
| Less search |                              |
|-------------|------------------------------|
| less /file.txt | search forward 'file.txt' |
| less ?file.txt | Reverse search 'file.txt' |
| n | jump to the next occurrence of the search term |
| N | jump to the previous event |
| q | quit |
| Useful few options |                   |
|--------------------|-------------------|
| less -N file.txt | Display line number |
| less +G file.txt | Open at the end of the file |
| less +F file.txt | Follow the additions if new content |
### The problem I encountered today:
Q1: Is it better than a cat?
A: cat used for short files, less long files or files that need to be searched.

## 2026-8-11
| command | function | my undestanding |
|---------|----------|-----------------|
| history | Check the lsit of commands you have used | View the history of uesd commands |
| !! | Execute the latest command again | Eexcute the most recent command |
| !number | Run by number | Use the command number in the history record |
| !cat | Run by prefix | Used to run the latest commands starting with . |
| Ctrl-R | Search your history | Start typing ant part of the commands you want, and the shell will display the most recent matches |
| history -c | Clear the current history it | Remove all entries from the history list in memory |
| history -w ~/.bash_history | Write the history into the file | Save the history of the current session to your history file. |
| history -d <offset> | Delete specific entrices | Delete a command through its historical number |
| clear | Clear the current interaction content |  |

## 2026-08-16
### CP
| Command | Function | My understanding |
|---------|----------|------------------|
| cp file1.txt file2.txt | Create a new copy while keeping the original file | Copy the content to a file or create a new file and copy its content |
| cp myfile /home/susie/ | To copy a file, you need to specify the source file and the target diretory or path | Copy the file to the specified source file and target diretorty or path | 
| cp file1 file2 file3 /home/susie | Copy multiple files to the directory | To copy multiple files to the same directory , first list all the sources and finally place them in the target directory |
| cp *.txt /home/susie/files | Copy all txt files at the current location to the directory | Use the universal character for batch copying, '*' Match any sequence of character,'?'Match any single character , '[]' Match any character within the parenrheses. |
| cp -r LSB_test/ /home/susie/LSB | Recursively copy the directory | Copy the dorectory and all its content to the specified directory. |
| cp -R LSB_test /home/susie/LSB | It has the same recursive effect in a typical Linux system. |  |
| cp -i  | Handle file overwriting | A confirmation prompt will be given before overwriting |
| cp -f  | Handle file overwriting | If necessary ,remove the target node for forced overwriting first |
| cp -n  | Handle file overwriting | Do not overwriting the existing files |
| cp -p  | Retain the original attributes of the file. | Retain mode,ownership(as much as possible), and timestamp. |
| cp -a  | It is often used for backup directory copies because it can recursively retain many attributers and copy. | The archiving mode helps to preserve the directory tree. |
| cp -u  | Copy only when the source file is updated than the target file or the target file does not exist. | This very usrful when refreshing the folder without rewriting  that are already the latest version. |
| cp -v  | Display the appearance of each file when it is copied. |  |
### The problem I encoutered today:
Q1: Why  can't cp copy directory?
A: The directory needs to be recursively copied.use 'cp -r source-dir destonation-dir.
Q2: Should cp-r or cp -a be used for backup?
A: 'cp -r' Used for simple recursice replication.It can be used 'cp -a' ,when you want a backup copy that saves more file attributes.

