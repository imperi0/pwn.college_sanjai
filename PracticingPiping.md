# Practicing Piping


### Duplicating piped data with tee

In this level i used tee to copy the data that is going to be sent to the next command.

<img width="570" height="152" alt="image" src="https://github.com/user-attachments/assets/1dc242c0-c087-4515-a402-c7d45d21faff" />

<img width="590" height="105" alt="image" src="https://github.com/user-attachments/assets/f991ec54-d5f5-471c-998d-ebf76657f76c" />

### Process substitution for input

<(command) runs command in a subshell and saves the output of that in a temp file like /dev/fd/63 and we can use <(cmd) in place of the file

<img width="568" height="65" alt="image" src="https://github.com/user-attachments/assets/a56f85a7-c6f9-4d55-80a2-4d1f8af7b6f1" />

### Writing to multiple programs

It’s like creating a temporary file that you can write to or read from, but instead of storing it on disk, the system streams the data directly into the command. The command then processes this data just like it would from a normal file. Once the command finishes, the temporary “file” disappears automatically.

This < (command) → runs the command and makes its output look like a file. Other commands can read from this “file” as if it were a normal file. It doesn’t actually create a real file on disk.

THis > (command) → creates a temporary pipe that acts like a file. Anything written into this “file” goes into the command as input. Again, no real file is created; it’s just a live connection

