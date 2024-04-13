
## HPCC Alias

```bash
alias vasp_energy='/home/jerschro/conda/bin/python3 /home/jerschro/Scripts/vasp/read_outcars_ssh.py'

```

## vasp_energy description

```
usage: vasp_energy [-h] [-f FILENAME] [-e] [-k] [-v] [-t] [-a SORTHIGH] [-d SORTLOW]

finds values from OUTCAR files

options:
  -h, --help            show this help message and exit
  -f FILENAME, --filename FILENAME
                        if the outcarfile has a different file name
  -e, --energy          turn off energy value print out
  -k, --kpoints         turn on kpoint values print out
  -v, --volume          turn on volume values print out
  -t, --time            turn on time values print out
  -a SORTHIGH, --sorthigh SORTHIGH
                        sort highest value first
  -d SORTLOW, --sortlow SORTLOW
                        sort lowest value first

written by jeremy schroeder 2-27-2024

```