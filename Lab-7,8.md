# Lab 7 & 8: Managing Permissions and Directories in Linux

## Objective
This lab focuses on learning how to manage directories, set permissions using symbolic and octal methods, and configure the `umask` for a user. You will create a directory, modify its permissions, and ensure proper access control for users and groups.

---

## Commands and Concepts Used

### 1. Create the `/home/consultants` Directory
To create the `/home/consultants` directory, use the `mkdir` command:
```bash
sudo mkdir /home/consultants
```

#### Screenshot:
![Creating the consultants directory](screenshots/mkdir_consultants.png)

---

### 2. Add Write Permission to the `consultants` Group
To grant write permission to the `consultants` group, use the `chmod` command with the symbolic method:
```bash
sudo chmod g+w /home/consultants
```

#### Explanation:
- `g+w`: Adds write (`w`) permission for the group (`g`).

#### Screenshot:
![Adding write permission to the group](screenshots/chmod_gw.png)

---

### 3. Restrict Access for Others
To restrict access for others to the `/home/consultants` directory, use the `chmod` command with the octal method:
```bash
sudo chmod 770 /home/consultants
```

#### Explanation:
- `770`: 
  - `7` (owner): Full permissions (read, write, execute).
  - `7` (group): Full permissions (read, write, execute).
  - `0` (others): No permissions.

#### Screenshot:
![Setting permissions using the octal method](screenshots/chmod_770.png)

---

### 4. Verify Directory Permissions
To check the permissions of the `/home/consultants` directory, use the `ls -ld` command:
```bash
ls -ld /home/consultants
```

#### Expected Output:
```
drwxrwx--- 2 root consultants 4096 Oct 10 12:34 /home/consultants
```

#### Screenshot:
![Verifying directory permissions](screenshots/ls_ld_consultants.png)

---

### 5. Modify the Default `umask` for the `operator1` User
The `umask` determines the default permissions for newly created files and directories. To modify the `umask` for the `operator1` user, follow these steps:

1. Switch to the `operator1` user:
   ```bash
   sudo su - operator1
   ```

2. Update the `umask` value in the user's shell configuration file (e.g., `.bashrc`):
   ```bash
   echo "umask 007" >> ~/.bashrc
   ```

3. Apply the changes:
   ```bash
   source ~/.bashrc
   ```

4. Verify the updated `umask`:
   ```bash
   umask
   ```

#### Explanation:
- `umask 007`: 
  - `0` (owner): Full permissions.
  - `0` (group): Full permissions.
  - `7` (others): No permissions.

#### Screenshot:
![Changing and verifying umask](screenshots/umask_change.png)

---

### 6. Confirm the Updated `umask`
To confirm that the new `umask` is applied, create a new file and directory, then check their permissions:
```bash
touch testfile
mkdir testdir
ls -l
```

#### Expected Output:
- File permissions: `-rw-rw----`
- Directory permissions: `drwxrwx---`

#### Screenshot:
![Confirming umask with new file and directory](screenshots/umask_confirm.png)

---

## Conclusion
In this lab, you practiced:
1. Creating directories and managing their permissions using symbolic and octal methods.
2. Restricting access to specific users and groups.
3. Configuring the `umask` to control default permissions for files and directories.

These techniques are essential for managing file systems and ensuring proper access control in Linux environments.

---