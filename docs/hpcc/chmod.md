## File Permissions Notes

``` title="/home/jerschro/Scripts/chmod/README"
How your files should be set up to read

First run commands in home directory:
setfacl -R -m g::r-x /home/eraider
setfacl -R -m g:ME:r-x /home/eraider
setfacl -R -m g:chem:r-x /home/eraider

Then run fix_ssh.sh to fix the .ssh directory
Then run modify_files.sh to turn all files not executable (.sh) to read only.

```


## fix_ssh.sh

### fix_ssh.sh path

```bash
cp /home/jerschro/Scripts/chmod/fix_ssh.sh .

```

### fix_ssh Description

```
usage: fix_ssh.sh [-h]

Fixes file permissions in .ssh folder. Script is meant to be run in home directory.

Written by Jeremy Schroeder 2-20-2024

```

## modify_files.sh

### modify_files.sh path

```bash
cp /home/jerschro/Scripts/chmod/modify_files.sh .

```

### modify_files Description

```
usage: modify_files.sh [-h]

Recursive script that reads all sub directories and fixes file permissions to all text files and executable scripts.

Written by Jeremy Schroeder 2-20-2024

```
