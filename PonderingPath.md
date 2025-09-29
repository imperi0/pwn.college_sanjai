# Pondering Path

### The PATH variable

In this level, you will disrupt the operation of the /challenge/run program.

<img width="440" height="120" alt="image" src="https://github.com/user-attachments/assets/a2d4278a-f5e0-45fe-8549-463dc4198bfc" />

### Setting PATH

 This level's /challenge/run will run the win command via its bare name, but this command exists in the /challenge/more_commands/ directory, which is not initially in the PATH.

<img width="481" height="100" alt="image" src="https://github.com/user-attachments/assets/552ab300-689a-4a33-8983-e4176773628d" />

### Finding Commands

In this challenge, we added a win command somewhere in your $PATH, but it won't give you the flag. Instead, it's in the same directory as a flag file that we made readable by you! You must find win (with the which command), and cat the flag out of that directory!

<img width="462" height="110" alt="image" src="https://github.com/user-attachments/assets/f9b01dc3-a155-4f1a-866c-05fca196f820" />

### Adding Commands

