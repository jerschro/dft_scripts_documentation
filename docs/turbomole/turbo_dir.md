
## Alias for HPCC

```bash
alias turbo_dir='/home/jerschro/conda/bin/python3 /home/jerschro/Scripts/turbomole/read_turbo_directories.py'

```

## Description of turbo_dir

```
usage: turbo_dir [-h] [-c] [-f FILTER_JOB_TYPE] [-d] [-r] [-n] [-e] [-t] [-q] [-p]

Finds Turbomole jobs in subdirectories and returns current information from them.

options:
  -h, --help            show this help message and exit
  -c, --control-info    Print detailed control file information. 
                        Job Information returned is [basis_set, func, conv, ri, marij, disp3] 
                        If you want control info printed out cleaner, use read_control script.
  -f FILTER_JOB_TYPE, --filter-job-type FILTER_JOB_TYPE
                        Filter job types. Supply string or list seperated by commas. 
                        'Turbomole job type' = [FILTER_JOB_TYPE keywords] 
                            'geo opt' = ['o','g','opt','geo opt','optimization'] 
                            'cosmos' = ['s','c','solvent','cosmo','cosmos','cosmoprep'] 
                            'freq' = ['f','freq','frequency'] 
                        Example Usage: 'turbo_dir --filter-job-type opt,freq
  -d, --done-jobs       Print only finished jobs.
  -r, --running-jobs    Print only currently running jobs.
  -n, --not-converged-jobs
                        Print only not converged jobs.
  -e, --export-to-csv   Print out return table in csv format.
                        Can use bash syntax to write to csv file. 
                        'turbo_dir --export-to-csv > readout.csv'
  -t, --export-to-tsv   Print out return table in tsv format. 
                        Can use bash syntax to write to tsv file. 
                        'turbo_dir --export-to-tsv > readout.tsv'
  -q, --show-frequencies
                        Turn on to show frequencies in vibspectrum file.
  -p, --print-debug     Turn on to print debug statements. Only for testing.

Written by Jeremy Schroeder 4-12-2024

```