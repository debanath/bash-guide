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

>If these steps don’t work, you may need assistance from your system administrator.