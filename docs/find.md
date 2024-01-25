# find

## basic syntax:
```bash
find [path] [options] [expression]
```

## examples

```bash
find .
```
You can use the ps command to display a list of your processes that are currently running and obtain additional information about those processes.

output:
```bash
find .
find .
.
./docs
./docs/ps.md
./docs/find.md
./README.md
./.git
./.git/config
./.git/objects
./.git/objects/pack
./.git/objects/info
./.git/HEAD
./.git/info
./.git/info/exclude
./.git/description
./.git/hooks
```

To find a file named “example.txt” in the home directory, you would use:

```bash
find ~ -name "example.txt"
```

## other flags

```bash
-mtime n 
```
Finds files based on modification time. `n` represents the number of days ago.

```bash
-exec command {} \; 
```
Executes a command on each file found.
