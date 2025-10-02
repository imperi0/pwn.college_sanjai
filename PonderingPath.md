# Pondering Path

## The PATH variable
In this level, you will disrupt the operation of the /challenge/run program.

### Solve
<img width="440" height="120" alt="image" src="https://github.com/user-attachments/assets/a2d4278a-f5e0-45fe-8549-463dc4198bfc" />

## Setting PATH
This level's /challenge/run will run the win command via its bare name, but this command exists in the /challenge/more_commands/ directory, which is not initially in the PATH.

### Solve
<img width="481" height="100" alt="image" src="https://github.com/user-attachments/assets/552ab300-689a-4a33-8983-e4176773628d" />

## Finding Commands
In this challenge, we added a win command somewhere in your $PATH, but it won't give you the flag. Instead, it's in the same directory as a flag file that we made readable by you! You must find win (with the which command), and cat the flag out of that directory!

### Solve
<img width="462" height="110" alt="image" src="https://github.com/user-attachments/assets/f9b01dc3-a155-4f1a-866c-05fca196f820" />

## Adding Commands
Previously, the win command that /challenge/run executed was stored in /challenge/more_commands. This time, win does not exist! Recall the final level of Chaining Commands, and make a shell script called win, add its location to the PATH, and enable /challenge/run to find it!

### Solve
In this challenge, I typed which cat. I added a win file with the text path and /flag. Next, I added it to the path using PATH and got the flag.

<img width="199" height="71" alt="image" src="https://github.com/user-attachments/assets/36bc79cb-ddba-434a-bc58-2540e0068ac2" />

<img width="431" height="147" alt="image" src="https://github.com/user-attachments/assets/e1eedf6f-e878-4291-9f6a-91c18c4c8862" />

## Hijacking Commands
You know that rm is searched for in the directories listed in the PATH variable. You have experience creating the win command when the previous challenge needed it. What else can you create?
Solve

### Solve

**Flag: pwn.college{wZ02JdzGk9BI0v2IOcqNjnZF_SG.QX3cjM1wiNzAzNzEzW}**

In this challenge, I typed echo $PATH and saw a list of directories and one by one checked if it had cat inside using ls and found it in /usr/bin. I added a rm file with the text /usr/bin/cat /flag. Next, I added it to the path using PATH="$PWD:$PATH" and got the flag

```bash
echo $PATH
nano rm
/usr/bin/cat /flag
PATH=$"PWD:$PATH"
/challenge/run
```
