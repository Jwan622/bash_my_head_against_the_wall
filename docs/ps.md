# PS

## ps -aux
```bash
ps -aux
```
You can use the ps command to display a list of your processes that are currently running and obtain additional information about those processes.

output:
```bash
ps aux
USER               PID  %CPU %MEM      VSZ    RSS   TT  STAT STARTED      TIME COMMAND
jwan             54966  18.0  0.9 410504576  74336   ??  S    16Jan24  28:08.12 /Applications/iTerm 2.app/Contents/MacOS/iTerm2
_windowserver      557  14.1  1.0 411717072  82432   ??  Rs   21Dec23 1038:22.87 /System/Library/PrivateFrameworks/SkyLight.framework/Resources/WindowServer -daemon
root               603   9.9  0.2 408422016  19744   ??  Ss   21Dec23 336:55.52 /usr/libexec/airportd
jwan             66384   9.3  3.8 418010272 321008   ??  R     1:45AM   1:42.65 /Applications/PyCharm.app/Contents/MacOS/pycharm .
jwan             62029   4.2  0.4 408512592  31840   ??  S    21Dec23 611:23.39 /System/Library/PrivateFrameworks/FileProvider.framework/Support/fileproviderd
jwan             85592   3.4  1.0 442891024  84064   ??  S    28Dec23 252:36.91 /Applications/Google Chrome.app/Contents/Frameworks/Google Chrome Framework.framework/Versions/120.0.
root                 1   3.4  0.2 408831040  13152   ??  Rs   21Dec23 424:48.13 /sbin/launchd
```



`ps` provides information about the currently running processes, including their PIDs. You can use ps with various options (-aux for example) to see CPU usage. The %CPU column shows the CPU usage.


