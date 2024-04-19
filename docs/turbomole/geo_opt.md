
## Alias for HPCC

```bash
alias geo_opt='bash /home/jerschro/Scripts/turbomole/geo_opt.sh'

```

## Description of geo_opt

```
usage: geo_opt.sh [-h] [-c CHARGE] [-s SCF_CONV] [-f FROZEN_ATOMS [FROZEN_ATOMS ...]] [-n] [--partition {quanah,nocona}]
                  [--nodes NODES] [--cpus CPUS] [--time TIME] [--mem_per_cpu MEM_PER_CPU]
                  STRUCTURE_FILEPATH JOB_NAME BASIS_SET DFT_FUNCTIONAL

Script that submits a TURBOMOLE geometry optimization calculation when arguments are supplied.

positional arguments:
  STRUCTURE_FILEPATH    Filepath to initial .xyz structure file or coord file.
  JOB_NAME              Name you want the job to be in the slurm file.
  BASIS_SET             Basis Set for calculation. Remember for example if you want SV(P), you need to type it as SV\(P\).
  DFT_FUNCTIONAL        Functional for calculation.

options:
  -h, --help            show this help message and exit
  -c CHARGE, --charge CHARGE
                        Initial charge for calculation. Default is 0.
  -s SCF_CONV, --scf_conv SCF_CONV
                        SCF Convergence criteria. Standard is 6 for optimization, 8 for frequency. Default is 6.
  -f FROZEN_ATOMS [FROZEN_ATOMS ...], --frozen_atoms FROZEN_ATOMS [FROZEN_ATOMS ...]
                        Type list of species you want to freeze. Default list is ['al','ti'].
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