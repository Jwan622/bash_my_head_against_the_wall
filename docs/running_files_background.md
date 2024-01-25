In Bash, the `&` at the end of a command is used to run the preceding command in the background as a job. When you execute `./trap_and_signal.sh &`, you are telling the shell to run the script `trap_and_signal.sh` in the background, which allows you to continue using the current shell session without having to wait for the script to finish executing.

Here's what happens when you run a script or any command with an ampersand (&):
- The script starts executing in a sub-process of the current shell session.
- The shell immediately returns a job ID and a process ID associated with the background task and gives you back the command prompt.
- You can continue to use the shell for other tasks while the background script is running.
- Any output from the background command will still be displayed in the shell, unless it is redirected to a file or another output stream.
- You can bring the job back to the foreground with the fg command if you need to interact with it.
- Running a script in the background is particularly useful for long-running tasks or for starting daemons and other services that run continuously.

example:
```bash
echo hi &
[1] 18820
hi
[1]+  Done                    echo hi
```

In Bash, when writing a while loop in a single line, you need to separate the commands with semicolons, and also you need to include a semicolon before done. Example:
```bash
while true; do echo 5 && sleep 3 && echo 6 && sleep 2; done &
```

This code will:
- create a background job
- Enter an infinite loop (while true;).
- echo 5 to print out the number 5.
- sleep 3 to pause execution for 3 seconds.
- echo 6 to print out the number 6.
- sleep 2 to pause execution for 2 seconds.
- Repeat the loop (done).


output is infinite unless you kill it:
```bash
02:31 $ while true; do echo 5 && sleep 3 && echo 6 && sleep 2; done &
[1] 27242
5
✔ ~/Desktop/programming/bash_my_head_against_the_wall [master|✚ 1]
02:31 $ 6
5
6
5jobs
jobs 
```


you need to kill it using the `kill` command after you find the background job with `jobs` command.
