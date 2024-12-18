# File Permissions in Linux

Understanding file permissions is crucial for managing access and ensuring system security. This guide will walk you through key concepts, commands, and examples for managing file permissions in Linux.

---

## 1. Viewing File Permissions

To see the permissions of a file, use the `stat` command:

```bash
stat <filename>
```
This will display detailed information about the file, including permissions in symbolic and numeric (octal) format.

## 2. Understanding Octal natation:

Permissions in Linux are represented in both symbolic and octal forms. Here’s how it works:

### Symbolic Values
* r (read): 4
* w (write): 2
* x (execute): 1
* \- (no permission): 0

### Structure of permissions:

Permissions are divided into three categories:

User (u): The owner of the file.
Group (g): The group associated with the file.
Other (o): Everyone else.

```sql
rwx -wx r-x
|   |   | 
User Group Other

```

## 3. Changing permissions with chmod:

The chmod command is used to modify file or directory permissions.

### Symbolic Mode
You can modify permissions for specific categories:

* u: User (owner)
* g: Group
* o: Others

exemples: 
```sh

chmod u+x <filename>         # Add execute permission to the user
chmod u+rwx <filename>       # Add read, write, and execute for the user
chmod o-w <filename>         # Remove write permission for others
chmod ug=rw,o= <filename>    # Set user and group to rw-, others to ---
# Resulting permission: rw-rw----
```
### Octal Mode:
Assign permissions directly using octal notation:

remember:
r = 4
w = 2
x = 1
\- = 0

* `chmod 755 myfile` set permission to: `rwxr-xr-x` (user: rwx, group: r-x, others: r-x) 
user : r = 4 + w = 2 + x = 1 = `7` group -> r = 4 + - = 0 + x = 1 = `5` others : r = 4 + - =0 + x = 1 = `5` 

### Recursive Permissions:
```sh
chmod -R 755 <directory>
```

## 4. Using find with Permissions:

You can change permissions for specific files or directories using find and chmod.

```sh 
find /home -type f -exec chmod 640 {} \;
```
```sh
* `/home`: Path to search.
* `-type f`: Matches files.
* `chmod 640 {}`: Applies 640 permissions to each file found.
```
## Change Directory Permissions:

* `-type d`: Matches directories.

```sh
find /home -type d -exec chmod 540 {} \;

```
Applies 540 permissions to each directory found

### Common Permission Sets
* `755`: Read, write, execute for user; read and execute for group and others.
* `644`: Read and write for user; read-only for group and others.