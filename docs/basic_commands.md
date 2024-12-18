# Basic Linux Commands

This guide provides a list of essential Linux commands to help you get started. These commands cover basic file operations, system navigation, and process management.

---



## 📂 Basic File and Directory Operations

### 1. List Files
```bash
ls
```
Options:
* `ls -l`: Detailed list with permissions, size, and timestamps.
* `ls -a`: Show hidden files.
* `ls -lh`: Human-readable file sizes.

## 2. Change Directory:

```sh
cd <directory>
```
* Examples:
- `cd /home`: Navigate to the /home directory.
- `cd ..`: Move up one directory level.
- `cd ~`: Go to the home directory.

### 3. Create a File:
```sh
touch <filename>
```
* Example:
- `touch myfile.txt`: Creates an empty file named myfile.txt.

### 4. Create a Directory:
```sh
mkdir <directory>
```
* Example:
- `mkdir myfolder`: Creates a folder named `myfolder`.

### 5. Remove a File or Directory:
* Remove a file:
```sh
rm <filename>
```
* Remove a directory and its contents:
```sh
rm -r <directory>
```
### 6. Copy Files and Directories:
```sh
cp <source> <destination>
```
- `cp file1.txt file2.txt`: Copy `file1.txt` to `file2.txt`.
- `cp -r folder1 folder2`: Copy `folder1` and its contents to `folder2`.
- `cp -p file copied`:    (preserve privilege access).

### 7. Move or Rename Files:

```sh
mv <source> <destination>
```
* Examples:
- `mv file.txt /tmp`: Move file.txt to /tmp.
* When the source and destination paths are in the same directory, mv functions as a renaming command:
- `mv oldname.txt newname.txt`: Rename oldname.txt to newname.txt.
* To move multiple files into a directory:
```sh
mv file1.txt file2.txt /path/to/destination/
```
mv can move entire directories:
```sh
mv /source/directory /destination/
```

## 🔍 Viewing Files and Directories:
### 1. View File Contents
* Display entire file:
```sh
cat <filename>
```
* View file with paging:
```sh
less <filename>
```
* View the first 10 lines:
```sh
head <filename>
```
* View the last 10 lines:
```sh
tail <filename>
```
