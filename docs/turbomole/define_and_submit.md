
## Alias for HPCC

```bash
alias geo_opt='bash /home/jerschro/Scripts/turbomole/run_define_and_submit_job.sh'

```

## Description of geo_opt

```
usage: geo_opt [-h] STRUCTURE_FILEPATH JOB_NAME BASIS_SET CHARGE DFT_FUNCTIONAL SCF_CONV

Script that submits a geometry optimization calculation when arguments are supplied.

positional arguments:
  STRUCTURE_FILEPATH    Filepath to initial .xyz structure file.
  JOB_NAME              Name you want the job to be in the slurm file.
  BASIS_SET             Basis Set for calculation. Remember for example if you want SV(P), you need to type it as SV\(P\).
  CHARGE                Initial charge for calculation. It is almost always 0.
  DFT_FUNCTIONAL        Functional for calculation.
  SCF_CONV              SCF Convergence criteria. Standard is 6 for optimization, 8 for frequency.

options:
  -h, --help            show this help message and exit.

Written by Jeremy Schroeder 4-12-2024

```