## Command Line Tutorial for Beginners (Windows Git Bash) - 30 Minutes

Welcome! This tutorial will teach you the essentials of navigating and managing files using the command line in Git Bash. You're now ready to start using your terminal.

### Part 1: Understanding Your Location (5 minutes)

**What is "pwd"?**
`pwd` stands for "print working directory." It tells you exactly where you are in the file system.

**Exercise 1.1:** Type this command in your terminal:
```bash
pwd
```

You should see a path like `/c/Users/YourUsername`. This is your current location. Congratulations—you just ran your first command!

**What is "ls"?**
`ls` stands for "list" and shows you all the files and folders in your current directory.

**Exercise 1.2:** Type:
```bash
ls
```

You should see a list of folders like `Desktop`, `Documents`, `Downloads`, etc. These are the items in your current directory.

**Combining commands with flags:**
A "flag" is an option you add to a command to change how it behaves. Flags usually start with `-` or `--`.

**Exercise 1.3:** Try:
```bash
ls -la
```

The `-l` flag shows a "long" format with more details (file sizes, dates). The `-a` flag shows hidden files (files that start with a dot). You can combine flags like this.

### Part 2: Moving Around Directories (8 minutes)

**What is "cd"?**
`cd` stands for "change directory." It's how you move from one folder to another.

**Exercise 2.1:** Navigate to your Desktop:
```bash
cd Desktop
```

Now type `pwd` to confirm you're on the Desktop. Type `ls` to see what's there.

**Going back up one level:**
`cd ..` moves you up one directory level (to the parent folder).

**Exercise 2.2:** Type:
```bash
cd ..
```

Type `pwd` and you should be back in `/c/Users/YourUsername`. Type `ls` to see your folders again.

**Using tab completion:**
This is a huge time-saver. Start typing a folder name and press `Tab`—Git Bash will auto-complete it for you.

**Exercise 2.3:** Type `cd Doc` and then press `Tab`. It should auto-complete to `cd Documents`. Press `Enter` to navigate there.

**The home directory shortcut:**
`cd ~` takes you directly to your home directory (`/c/Users/YourUsername`) from anywhere.

**Exercise 2.4:** Try:
```bash
cd ~
pwd
```

### Part 3: Creating and Viewing Files (7 minutes)

**What is "touch"?**
`touch` creates a new empty file.

**Exercise 3.1:** Type:
```bash
touch myfile.txt
```

Now type `ls` and you should see `myfile.txt` in the list. Congratulations—you created a file!

**What is "mkdir"?**
`mkdir` stands for "make directory" and creates a new folder.

**Exercise 3.2:** Type:
```bash
mkdir my_folder
```

Type `ls` and you should see your new folder `my_folder`.

**What is "cat"?**
`cat` displays the contents of a file. Since we just created an empty file, it won't show much.

**Exercise 3.3:** Type:
```bash
cat myfile.txt
```

It will be empty (or show nothing), which is expected. Let's skip to the next section.

### Part 4: Copying, Moving, and Removing Files (7 minutes)

**What is "cp"?**
`cp` stands for "copy." The syntax is `cp source destination`.

**Exercise 4.1:** Copy your file:
```bash
cp myfile.txt myfile_copy.txt
```

Type `ls` and you should see both `myfile.txt` and `myfile_copy.txt`.

**What is "mv"?**
`mv` stands for "move." You can use it to move a file to another location or rename it.

**Exercise 4.2:** Rename your copied file:
```bash
mv myfile_copy.txt myfile_renamed.txt
```

Type `ls` and the file should now be called `myfile_renamed.txt`.

**Exercise 4.3:** Move the file into your folder:
```bash
mv myfile_renamed.txt my_folder/
```

Type `ls` and the file should no longer be in the current directory. Type `ls my_folder/` and the file should be there.

**What is "rm"?**
`rm` stands for "remove" and deletes a file. **Warning:** There's no trash/undo—it's gone forever!

**Exercise 4.4:** Delete the file:
```bash
rm my_folder/myfile_renamed.txt
```

Type `ls my_folder/` and it should be empty. Type `rm -r my_folder` to remove the folder itself (the `-r` flag means "recursive," which removes folders and everything inside them).

### Part 5: Getting Help (3 minutes)

**What is "help" and "man"?**
Every command has documentation. You can view it with `man` (manual) or `command --help`.

**Exercise 5.1:** Type:
```bash
ls --help
```

You'll see all the flags available for `ls`. This is useful when you forget what a command does or what options it has.

**Exercise 5.2:** Try:
```bash
man pwd
```

This shows the manual for `pwd`. Press `q` to exit the manual.

### Summary Cheat Sheet

| Command | What it does | Example |
|---------|-------------|---------|
| `pwd` | Print working directory | `pwd` |
| `ls` | List files and folders | `ls` or `ls -la` |
| `cd` | Change directory | `cd Desktop` or `cd ..` |
| `mkdir` | Make a new folder | `mkdir my_folder` |
| `touch` | Create a new empty file | `touch myfile.txt` |
| `cp` | Copy a file | `cp file.txt file_copy.txt` |
| `mv` | Move or rename a file | `mv old_name.txt new_name.txt` |
| `rm` | Remove a file | `rm myfile.txt` |
| `rm -r` | Remove a folder | `rm -r my_folder` |
| `cat` | View file contents | `cat myfile.txt` |
| `command --help` | Get help on a command | `ls --help` |

### Final Exercise

Now let's practice everything together:

```bash
cd ~
mkdir practice
cd practice
touch file1.txt
touch file2.txt
ls
cp file1.txt file1_backup.txt
mv file2.txt file2_renamed.txt
ls -la
cd ..
rm -r practice
pwd
```

**Congratulations!** You've completed the beginner command-line tutorial. You now understand:
- How to find your location (`pwd`)
- How to list files (`ls`) and navigate directories (`cd`)
- How to create files and folders (`touch`, `mkdir`)
- How to copy, move, and delete files (`cp`, `mv`, `rm`)
- How to use flags to modify command behavior
- How to get help (`--help`, `man`)

You're ready to move on to the next sections of this tutorial!
