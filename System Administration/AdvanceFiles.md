

## Disk commands

### Disk usage
```bash
du <options>
```
- Allow a user to his/her usage including subdirectories
- by default, the disk usage in presented in **1024** byte blocks

### Disk statistics
```bash
df <options>
```
- shows the disk statistics o fa file system
- can show used and avialable space and percentage usage

_du -> how much space files are using_
_df -> how much space the disk has left_

## Advance File commands

### Creating alternative names of a file or directory
```bash
In [target file] [link name]
```
_2 Types_: **Hard link** (default) or **Soft Link** (-s) 

#### Hard Link [Default]
- The meta data is edited to add a new file name for the same file 
- Not able to linke across file systems
- File is accessible as long as at least 1 hard link exists
#### Soft ile [-s]
- New file -> link the file to the target 
- Linkable across file systems
- easy to identify when listing uisng ls cmd 
- Breaks when original file is deleted


### File Permission
- way to add security in the system
- Each file in the Unix system has an owner and Permission
    - Using a _**USER ID**_
- A group may have an ownership of a file 
    - useful for priviledge management 
- The owner has access to the file and modieifies the perms 

#### Anatomy of permission data
```bash
-rwxr--r-- 1 user100 student  51 Jun 22 15:01 hello.py
### -rwx r-- r-- = the file permisions [owner] [group] [others]
### [-] type | could be => [-] files , [d] direcories , [l] symlink 
### [rwx] means the owner has read write and execute
### [r--] the group can only read
### [r--] others can only read
### user100 owner 
### student -> the name of the group [group ownership]
```
#### The octal bits and assigning them
 R is for **read** | W is for **write** | X is for **execute** 

##### For File 
```bash
chmod vars file
```
##### For directories
```bash
chmod -R vars dir/
```

#### These options can be shown as numbers
**Perms Number conversion**
read r      4
write w     2
exec x      1 

**Common Number Combinations**
7   rwx 
6   rw- 
5   r-x 
4   read only


**Common Number perms**
777 full access
755 Executable programs
644 normal files
700 owner only files [private]




