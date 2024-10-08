# Preliminary Exercise in Bash
An exercise in basic Bash scripting. The purpose is to write a script that, upon invocation, shows the time and date, lists all logged-in users, and gives the system uptime. The script then saves this information to a logfile. 

The exercise follows [Chapter 2.2](https://linux.die.net/abs-guide/prelimexer.html) of the book [*Advanced Bash-Scripting Guide*](https://linux.die.net/abs-guide/index.html) by Mendel Cooper.

## Things to remember
<details>

**chmod 555 scriptname** gives everyone read/execute permission. Read/execute permission is required to successfully run scripts.

**./scriptname.** or **bash scriptname** runs the script. It is necessary to indicate the current directory (./) in the first command, as it is not included in a user's $PATH by default.

**sudo mv scriptname /usr/local/bin/scriptname** to move the script to the /usr/local/bin/ location and make it available systemwide. It can then be invoked with **bash scriptname** from any location.

[Book Reference](https://linux.die.net/abs-guide/invoking.html)
</details>

## Script
<details>
</details>
