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

