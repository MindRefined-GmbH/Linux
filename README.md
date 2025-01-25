# Linux Cheat Sheet

#### TODO
- [ ] Table of contents

#

### `whoami`
#### Print the username associated with the current effective user ID.
>More information: https://www.gnu.org/software/coreutils/manual/html_node/whoami-invocation.html.

Display currently logged username:
```
whoami
```

Display the username after a change in the user ID:
```
sudo whoami
```

#

### `pwd`
#### Print name of current/working directory.
>More information: https://www.gnu.org/software/coreutils/manual/html_node/pwd-invocation.html.

Print the current directory:
```
pwd
```

Print the current directory, and resolve all symlinks (i.e. show the "physical" path):
```
pwd -P
```

#

### `ls`
#### List directory contents.
>More information: https://www.gnu.org/software/coreutils/manual/html_node/ls-invocation.html.

List files one per line:
```
ls -1
```


List **a**ll files, including hidden files:
```
ls -a
```

List files with a trailing symbol to indicate file type (`directory/`, `symbolic_link@`, `executable*`, etc.):
```
ls -F
```

List **a**ll files in **l**ong format (permissions, ownership, size, and modification date):
```
ls -la
```

List files in **l**ong format with size displayed using **h**uman-readable units (KiB, MiB, GiB):
```
ls -lh
```

List files in **l**ong format, sorted by **S**ize (descending) **R**ecursively:
```
ls -lSR
```

List files in **l**ong format, sorted by **t**ime the file was modified and in **r**everse order (oldest first):
```
ls -ltr
```

Only list **d**irectories:
```
ls -d */
```
<br>

> **Info:** Use the above commands with for a better experience: `--color=auto` and `--group-directories-first`


#

### `cd`
#### Change the current working directory.
>More information: https://manned.org/cd.

Go to the specified directory:
```
cd path/to/directory
```

Go up to the parent of the current directory:
```
cd ..
```

Go to the home directory of the current user:
```
cd
```

Go to the home directory of the specified user:
```
cd ~username
```

Go to the previously chosen directory:
```
cd -
```

Go to the root directory:
```
cd /
```

#

### `mkdir`
#### Create directories and set their permissions.
>More information: https://www.gnu.org/software/coreutils/manual/html_node/mkdir-invocation.html.

Create specific directories:
```
mkdir path/to/directory1 path/to/directory2 ...
```

Create specific directories and their parents if needed:
```
mkdir -p|--parents path/to/directory1 path/to/directory2 ...
```

Create directories with specific permissions:
```
mkdir -m|--mode rwxrw-r-- path/to/directory1 path/to/directory2 ...
```

#

### `rm`
#### Remove files or directories.
See also: `rmdir`
>More information: https://www.gnu.org/software/coreutils/manual/html_node/rm-invocation.html.

Remove specific files:
```
rm path/to/file1 path/to/file2 ...
```

Remove specific files ignoring nonexistent ones:
```
rm -f path/to/file1 path/to/file2 ...
```

Remove specific files interactively prompting before each removal:
```
rm -i path/to/file1 path/to/file2 ...
```

Remove specific files printing info about each removal:
```
rm -v path/to/file1 path/to/file2 ...
```

Remove specific files and directories recursively:
```
rm -r path/to/file_or_directory1 path/to/file_or_directory2 ...
```

#


