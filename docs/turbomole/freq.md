
## Alias of freq

``` bash
alias freq='bash /home/jerschro/Scripts/turbomole/freq.sh'

```

## Description of freq

```
usage: freq.sh [-h] [--vib_freq_method {n,N,NumForce,a,aoforce}] [-s SCF_CONV] [-n] [--partition {quanah,nocona}]
               [--nodes NODES] [--cpus CPUS] [--time TIME] [--mem_per_cpu MEM_PER_CPU]
               GEO_OPT_DIR JOB_NAME

Script that submits a frequency calculation when arguments are supplied.

positional arguments:
  GEO_OPT_DIR           Filepath to initial .xyz structure file or coord file.
  JOB_NAME              Name you want the job to be in the slurm file.

options:
  -h, --help            show this help message and exit
  --vib_freq_method {n,N,NumForce,a,aoforce}
                        What Frequency function you want.
  -s SCF_CONV, --scf_conv SCF_CONV
                        SCF Convergence criteria. Standard is 6 for optimization, 8 for frequency. Default is 8.
  -n, --no_sbatch       Stop auto submission of geo_opt job.
  --partition {quanah,nocona}
                        Partition of where the job should be submitted. Default is quanah.
  --nodes NODES         Nodes on partition. Default is 1.
  --cpus CPUS           Total CPUS. Default is 36.
  --time TIME           Total time limit for job. Default is 48:00:00
  --mem_per_cpu MEM_PER_CPU
                        Total time limit for job. Default is 5200MB

Written by Jeremy Schroeder 4-18-2024.
    Implements expect scripts and ideals from Tristan Fisher.
    Uses bash library: https://github.com/nhoffman/argparse-bash

```
