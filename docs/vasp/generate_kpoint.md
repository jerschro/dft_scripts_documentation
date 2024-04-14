
### generate_kpoint_test.sh path

``` bash
cp /home/jerschro/Scripts/vasp/generate_kpoint_test.sh .

```

## generate_kpoint_test.sh Description

```
usage: generate_kpoint_test.sh [-h]

Script that generates kpoint test directories for vasp and submits jobs (if uncommented).

generate_kpoint_test.sh reads orig/ directory in submit directory. Below are files needed in orig/
  -POSCAR
  -INCAR
  -$slurm_file
  -POTCAR

defined variables (located in top of file):
  start                 Initial kpoint integer value.
  end                   Last kpont integer value.
  jobname               Jobname added to slurm_file.
  slurm_file            Name of slurm_file. Should have JOB_NAME where you want the jobname.

current variables defined in top of file:
  $start = 1
  $end = 10
  $jobname = ex_kpoint_test
  $slurm_file = run_vasp.sh

options:
  -h, --help            show this help message and exit.

Written by Jeremy Schroeder 4-13-2024


```

## generate_kpoint_test.sh Example Usage

<details>
<summary>Example of generate_kpoint_test.sh Terminal Output</summary>

```title="quanah:/kpoint_test_example$ bash generate_kpoint_test.sh"
 starting kpoint test program
 checking orig folder
 orig folder is good, starting to make kpoint folders
 kpoints 1x1x1 being created
 kpoints 1x1x1 dir done
 kpoints 2x2x2 being created
 kpoints 2x2x2 dir done
 kpoints 3x3x3 being created
 kpoints 3x3x3 dir done
 kpoints 4x4x4 being created
 kpoints 4x4x4 dir done
 kpoints 5x5x5 being created
 kpoints 5x5x5 dir done
 kpoints 6x6x6 being created
 kpoints 6x6x6 dir done
 kpoints 7x7x7 being created
 kpoints 7x7x7 dir done
 kpoints 8x8x8 being created
 kpoints 8x8x8 dir done
 kpoints 9x9x9 being created
 kpoints 9x9x9 dir done
 kpoints 10x10x10 being created
 kpoints 10x10x10 dir done
 finished kpoint job submission yayyy
```
</details>


<details>
<summary>Example of generate_kpoint_test.sh File Creation</summary>

```title="quanah:/kpoint_test_example$ ls *"
generate_kpoint_test.sh

10x10x10:
INCAR  KPOINTS  POSCAR  POTCAR  run_vasp.sh

1x1x1:
INCAR  KPOINTS  POSCAR  POTCAR  run_vasp.sh

2x2x2:
INCAR  KPOINTS  POSCAR  POTCAR  run_vasp.sh

3x3x3:
INCAR  KPOINTS  POSCAR  POTCAR  run_vasp.sh

4x4x4:
INCAR  KPOINTS  POSCAR  POTCAR  run_vasp.sh

5x5x5:
INCAR  KPOINTS  POSCAR  POTCAR  run_vasp.sh

6x6x6:
INCAR  KPOINTS  POSCAR  POTCAR  run_vasp.sh

7x7x7:
INCAR  KPOINTS  POSCAR  POTCAR  run_vasp.sh

8x8x8:
INCAR  KPOINTS  POSCAR  POTCAR  run_vasp.sh

9x9x9:
INCAR  KPOINTS  POSCAR  POTCAR  run_vasp.sh

orig:
INCAR  POSCAR  POTCAR  POTCAR  run_vasp.sh


```
</details>

<details>
<summary>Example of generate_kpoint_test.sh KPOINTS Files</summary>

```title="quanah:/kpoint_test_example$ head */KPOINTS"
==> 10x10x10/KPOINTS <==
Automatic
 0
Monkhorst
 10  10  10
 0. 0. 0.

==> 1x1x1/KPOINTS <==
Automatic
 0
Monkhorst
 1  1  1
 0. 0. 0.

==> 2x2x2/KPOINTS <==
Automatic
 0
Monkhorst
 2  2  2
 0. 0. 0.

==> 3x3x3/KPOINTS <==
Automatic
 0
Monkhorst
 3  3  3
 0. 0. 0.

==> 4x4x4/KPOINTS <==
Automatic
 0
Monkhorst
 4  4  4
 0. 0. 0.

==> 5x5x5/KPOINTS <==
Automatic
 0
Monkhorst
 5  5  5
 0. 0. 0.

==> 6x6x6/KPOINTS <==
Automatic
 0
Monkhorst
 6  6  6
 0. 0. 0.

==> 7x7x7/KPOINTS <==
Automatic
 0
Monkhorst
 7  7  7
 0. 0. 0.

==> 8x8x8/KPOINTS <==
Automatic
 0
Monkhorst
 8  8  8
 0. 0. 0.

==> 9x9x9/KPOINTS <==
Automatic
 0
Monkhorst
 9  9  9
 0. 0. 0.
```

</details>