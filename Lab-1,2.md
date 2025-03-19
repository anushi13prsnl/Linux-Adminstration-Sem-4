# Lab 1 & 2: Managing Files and Directories in Linux

## Objective
The goal of this lab is to practice creating files and directories using Linux commands. We will explore how to use the `touch` command to create files and the `mkdir` command to create multiple directories in one go.

## Commands Overview
### Creating Multiple Files
To generate multiple files with specific names, the `touch` command can be combined with **brace expansion**. The syntax is as follows:
```bash
touch song{1..6}.mp3 snap{1..6}.jpg film{1..6}.avi
```
#### Explanation:
- `song{1..6}.mp3`: Expands to `song1.mp3 song2.mp3 song3.mp3 song4.mp3 song5.mp3 song6.mp3`
- `snap{1..6}.jpg`: Expands to `snap1.jpg snap2.jpg snap3.jpg snap4.jpg snap5.jpg snap6.jpg`
- `film{1..6}.avi`: Expands to `film1.avi film2.avi film3.avi film4.avi film5.avi film6.avi`
- The `touch` command ensures that all these files are created in the current working directory.

### Creating Multiple Directories
To create several directories at once, the `mkdir` command is used:
```bash
mkdir friends family work
```
#### Explanation:
- The `mkdir` command is used to create directories.
- Providing multiple directory names separated by spaces allows you to create them all at once.
- In this example, the directories `friends`, `family`, and `work` are created.

## Checking the Created Files and Directories
After executing the above commands, use the `ls` command to display the created files and directories:
```bash
ls
```
Expected output:
```
friends  family  work  song1.mp3  song2.mp3  song3.mp3  song4.mp3  song5.mp3  song6.mp3  snap1.jpg  snap2.jpg  snap3.jpg  snap4.jpg  snap5.jpg  snap6.jpg  film1.avi  film2.avi  film3.avi  film4.avi  film5.avi  film6.avi
```

### Screenshots
Below are screenshots showcasing the execution of the commands:

#### 1. Executing the `touch` and `mkdir` commands:
![Creating Files and Directories](screenshots/create_files_dirs.png)

#### 2. Displaying the created files and directories:
![Listing Files](screenshots/list_files.png)

## Conclusion
In this lab, we learned how to efficiently create multiple files using `touch` with brace expansion and multiple directories using `mkdir`. These commands are essential for effective file and directory management in Linux.