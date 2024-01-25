# chmod

In Unix operating systems, the chmod command is used to change the access mode of a file. The name is an abbreviation of change mode. Which states that every file and directory has a set of permissions that control the permissions like who can read, write or execute the file. In this the permissions have three categories: read, write, and execute simultaneously represented by `r`, `w` and `x`. These letters combine together to form a specific permission for a group of users.

## syntax

```bash
chmod [options] [mode] [File_name] 
```
Options: Optional flags that modify the behavior of the chmod command.
Mode: The permissions to be set, represented by a three-digit octal number or symbolic notation (e.g., u=rw,go=rx).
File_name: The name of the file or directory for which the permissions are to be changed.


### Options Available in chmod Command Linux

`-R`	Apply the permission change recursively to all the files and directories within the specified directory.
`-v`	It will display a message for each file that is processed. while indicating the permission change that was made.
`-c`	It works same as `-v` but in this case it only displays messages for files whose permission is changed.
`-f`	It helps in avoiding display of error messages.
`-h`	Change the permissions of symbolic links instead of the files they point to.


### Modes in chmod Command in Linux
The “mode” helps in setting new permissions that have to be applied to files or directories.

This mode can be specified in several ways, we will discuss two modes: Symbolic and Octal mode. 

1) Symbolic mode
If we talk about symbolic mode, we can say that it is the most common method used for specifying fir permissions. In this we have to make a combination of letters and operators to set or tell what to do with permissions.

The following operators can be used with the symbolic mode:
Operators	Definition
`+`	        Add permissions
`-`	        Remove permissions
`=`	        Set the permissions to the specified values


The following letters that can be used in symbolic mode:
Letters	Definition
`r`	    Read permission
`w`	    Write permission
`x` 	Execute permission


The following Reference that are used:
| Reference | Class                       |
|-----------|-----------------------------|
| u         | Owner                       |
| g         | Group                       |
| o         | Others                      |
| a         | All (owner, groups, others) |


### Examples of Using the Symbolic mode:
Read, write and execute permissions to the file owner:
```bash
chmod u+rwx [file_name]
```

Remove write permission for the group and others:
```bash
chmod go-w [file_name]
```

Read and write for Owner, and Read-only for the group and other:
```bash
chmod u+rw,go+r [file_name]
```

2) Octal mode
It is also a method for specifying permissions. In this method we specify permission using three-digit number. Where..

> First digit specify the permission for Owner.
Second digit specify the permission for Group. 
Third digit specify the permission for Others. The digits 
NOTE: The digits are calculated by adding the values of the individual permissions.


| Value | Permission         |
|-------|--------------------|
| 4     | Read Permission    |
| 2     | Write Permission   |
| 1     | Execute Permission |


### Examples of Using the Octal mode:
Suppose if we to give read and write permission to the file Owner. Read, write and executable permission to the Group. Read-only permission to the Other. Remember 6 = 4 + 2; we add an octal mode. Then our command would be.
```bash
chmod 674 [file_name]
```
Here.

6 represent permission of file Owner which are (rw).
7 represent permission of Group which are (rwx).
4 represent permission of Other which is (r).
