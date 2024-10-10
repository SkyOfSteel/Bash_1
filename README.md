# Preliminary Exercise in Bash
An exercise in basic Bash scripting. The purpose is to write a script that, upon invocation, shows the time and date, lists all logged-in users, and gives the system uptime. The script then saves this information to a logfile. 

The exercise follows [Chapter 2.2](https://linux.die.net/abs-guide/prelimexer.html) of the book [*Advanced Bash-Scripting Guide*](https://linux.die.net/abs-guide/index.html) by Mendel Cooper.

## Things to Remember
<details>

**chmod 555 scriptname** gives everyone read/execute permission. Read/execute permission is required to successfully run scripts.

**./scriptname.** or **bash scriptname** runs the script. It is necessary to indicate the current directory (./) in the first command, as it is not included in a user's $PATH by default.

**sudo mv scriptname /usr/local/bin/scriptname** to move the script to the /usr/local/bin/ location and make it available systemwide. It can then be invoked with **bash scriptname** from any location.

[Book Reference](https://linux.die.net/abs-guide/invoking.html)
</details>

## Script
<details>
  
```
#!bin/bash
LOGFILE=~/script.log
echo 'Current date is' $(date) | tee $LOGFILE
echo 'Currently logged in users are:' | tee -a $LOGFILE
who | tee -a $LOGFILE
echo 'The system uptime is:' $(uptime) | tee -a $LOGFILE
```

![image](https://github.com/user-attachments/assets/1946f132-5ab8-453b-bd6d-fa2601d44ef9)

</details>

## Additional Considerations
<details>

**tee** is a special command to simultaneously display the output on screen and write it to a file. 

**tee -a** makes the command append the text instead of overwriting it.

However, using the stdout is also possible to write data into the log without displaying it on screen. In this case, a pipe is not needed.

echo 'Current date is' $(date) 1>$LOGFILE

</details>
