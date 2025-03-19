# Lab 5 & 6: Editing Files in Linux Using Vim and Nano

## Objective
The aim of this lab is to get hands-on experience with two widely used text editors in Linux: **Vim** and **Nano**. You will edit the `editing_final_lab.txt` file, use Vim's visual mode for text manipulation, and perform specific tasks like removing characters and retaining selected portions of text.

---

## Commands and Concepts Used

### 1. Preparing the Lab File
To begin, ensure the `editing_final_lab.txt` file exists. If it is not present, create it using:
```bash
touch editing_final_lab.txt
```

To simplify file access, store its path in a shell variable:
```bash
lab_file="editing_final_lab.txt"
```

#### Screenshot:
![Setting the shell variable](screenshots/set_lab_file.png)

---

### 2. Editing with Nano
Nano is a straightforward and beginner-friendly text editor. Open the file in Nano using:
```bash
nano $lab_file
```

#### Screenshot:
![Opening Nano](screenshots/nano_open.png)

#### Tasks in Nano:
1. Add the following lines to the file:
   ```
   This is the first line of the file.
   This is the second line of the file.
   This is the third line of the file.
   ```

2. Save the changes by pressing `CTRL + O`, and exit Nano by pressing `CTRL + X`.

#### Screenshot:
![Saving and exiting Nano](screenshots/nano_save_exit.png)

---

### 3. Editing with Vim
Vim is a versatile and powerful text editor. Open the file in Vim using:
```bash
vim $lab_file
```

#### Screenshot:
![Opening Vim](screenshots/vim_open.png)

#### Tasks in Vim:
1. **Activate Visual Mode**:
   - Place the cursor on the first line.
   - Press `v` to enter visual mode.

#### Screenshot:
![Entering Visual Mode](screenshots/vim_visual_mode.png)

2. **Delete the Last Seven Characters of the First Line**:
   - While in visual mode, highlight the last seven characters of the first line.
   - Press `d` to delete the selected text.

3. **Keep Only the First Four Characters of the First Line**:
   - Move the cursor to the start of the first line.
   - Press `4l` to move the cursor to the fourth character.
   - Press `v` to enter visual mode, then highlight the rest of the characters after the fourth one.
   - Press `d` to delete the highlighted portion.

4. **Save and Exit**:
   - Press `ESC` to switch to command mode.
   - Type `:wq` and press `Enter` to save the file and exit Vim.

#### Screenshot:
![Saving and exiting Vim](screenshots/vim_save_exit.png)

---

## Verifying Command Execution
To confirm the changes, display the file's contents using:
```bash
cat $lab_file
```

#### Screenshot:
![Verifying file contents](screenshots/cat_file.png)

### Expected Output:
If the file initially contained:
```
This is the first line of the file.
This is the second line of the file.
This is the third line of the file.
```

After editing with Vim, the first line should appear as:
```
This
```

---

## Conclusion
In this lab, you explored how to use **Nano** and **Vim** for editing files in Linux. You practiced essential text manipulation techniques in Vim, such as entering visual mode, deleting specific characters, and retaining selected portions of text. These skills are fundamental for efficient file editing and Linux scripting.

---