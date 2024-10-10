# Guide to Getting Bash
### 1. Checking Your Current Shell
To find out which shell you are using, run:
```bash
echo $SHELL
```
This command will display one of the following:
- `sh` (Bourne shell)
- `csh` (C shell)
- `ksh` (Korn shell)
- `bash` (Bash shell)
If you see any other result (like `tcsh`), you may not be using bash.
### 2. Switching to Bash
To check if bash is available on your system, type:
```bash
bash
```
If a new prompt like `bash3 $` appears, bash is installed. To return to your current shell, type:
```bash
exit
```
> [!NOTE]
> If you get a “not found” message, bash might not be installed. Contact your system administrator to see if it's installed in an inaccessible directory, or proceed with installing it if necessary.
### 3. Making Bash Your Default Shell
You can temporarily start bash from any other shell by typing `bash`, but it’s better to make it your default login shell.

#### Steps to install bash as your login shell:

1. Find bash on your system
Use one of the following commands to locate where bash is installed:
    ```bash
    whereis bash
    whence bash
    which bash
    ```
    > If these don't work, try the following complex command:
    ```bash
    grep bash /etc/passwd | awk -F: '{print $7}' | sort -u
    ```

1. Set bash as your login shell
Once you’ve identified where bash is installed (e.g., `/bin/bash` or `/usr/local/bin/bash`), run:
    ```bash
    chsh /usr/local/bin/bash
    ```
    (Replace `/usr/local/bin/bash` with the correct path found in the previous step.)

1. Confirm the Change
    You may be prompted for your password. After entering it, log out and back in to start using bash as your default shell.
> [!NOTE]
> If these steps don’t work, you may need assistance from your system administrator.

# Files in UNIX :page_facing_up:

Although not all command arguments are files, files are fundamental in any UNIX system. Files can hold various types of information, and three main types are crucial:

1. **Regular Files**  
    - Also known as _text files_.
    - These contain readable characters and are the most common type of file.
    - Example: This guide was created using several regular files, which hold text and human-readable formatting instructions for processing.

2. **Executable Files**  
    - Also referred to as _programs_.
    - These are files that can be executed as commands. Some are not readable by humans, while others, like _shell scripts_, are special text files that can be run by the system.
    - The shell itself (e.g., `bash`) is a non-human-readable executable file.

3. **Directories**  
    - Directories are like _folders_ that can contain other files and subdirectories.
    - They organize files into a hierarchical structure, helping to manage and access files efficiently.

These file types form the backbone of working in a UNIX system, allowing users to store, execute, and organize data effectively.