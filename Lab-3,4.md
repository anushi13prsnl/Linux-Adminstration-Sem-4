# Lab 3 & 4: Exploring man Pages, Searching Commands, and Using Brace Expansion in Linux

## Objective
The purpose of this lab is to learn how to use Linux manual (`man`) pages, search for commands associated with `ext4`, and utilize **brace expansion** to generate custom strings of characters.

## Commands Used

### Viewing the Manual Page for `gedit`
To access the manual page for `gedit`, use the following command:
```bash
man gedit
```
#### Explanation:
- The `man` command opens the manual page for a specified command.
- `gedit` is a text editor commonly used in the GNOME desktop environment.

### Searching for Commands Related to `ext4`
To locate commands associated with the `ext4` file system, use:
```bash
man -k ext4
```
#### Explanation:
- The `-k` option searches through manual page descriptions for the specified keyword (`ext4`).
- This is useful for finding commands related to managing or tuning the ext4 file system.

### Using Brace Expansion
Brace expansion is a feature that allows you to generate strings of characters efficiently. It is particularly useful for creating lists or sequences.

#### Example 1: Creating a List of Strings
```bash
echo file_{A,B,C}.txt
```
**Output:**
```
file_A.txt file_B.txt file_C.txt
```

#### Example 2: Creating a Sequence of Numbers
```bash
echo number_{1..5}
```
**Output:**
```
number_1 number_2 number_3 number_4 number_5
```

#### Example 3: Combining Text with Brace Expansion
```bash
echo backup_{2024..2026}_v{1..3}.zip
```
**Output:**
```
backup_2024_v1.zip backup_2024_v2.zip backup_2024_v3.zip backup_2025_v1.zip backup_2025_v2.zip backup_2025_v3.zip backup_2026_v1.zip backup_2026_v2.zip backup_2026_v3.zip
```

## Verifying Command Execution
To confirm the execution of the above commands, use:
```bash
man gedit
man -k ext4
echo file_{A,B,C}.txt
echo number_{1..5}
```

### Screenshots
Below are screenshots illustrating the execution of the commands:

#### 1. Viewing the `gedit` manual page:
![gedit man page](screenshots/mangedit.png)
![gedit man page](screenshots/gedit_man.png)

#### 2. Searching for commands related to `ext4`:
![Searching ext4](screenshots/search_ext4.png)

#### 3. Demonstrating brace expansion:
![Brace Expansion](screenshots/brace_expansion.png)

## Conclusion
In this lab, we explored how to use `man` pages, searched for commands related to `ext4` using `man -k`, and demonstrated the versatility of **brace expansion** for generating multiple strings. These techniques are essential for efficient command-line operations and scripting in Linux.