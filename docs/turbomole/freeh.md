
## auto_freeh.sh

### auto_freeh.sh path

``` bash
cp /home/jerschro/Scripts/turbomole/freeh/auto_freeh.sh .

```

### auto_freeh.sh Description

```
usage: auto_freeh.sh [-h]

Shell for automating CSV_freeh.sh in multiple turbomole frequency directories.

Written by Jeremy Schroeder 4-13-2024

```

## CSV_thermo.sh

### CSV_freeh.sh path

``` bash
cp /home/jerschro/Scripts/turbomole/freeh/CSV_freeh.sh .

```

### CSV_freeh.sh Description

```
usage: CSV_freeh.sh [-h] CSV_FILENAME TSTART TEND NUMT [INDEX_INT_LIST (optional)]

Script that submits a geometry optimization calculation when arguments are supplied.

positional arguments:
  CSV_FILENAME          Output .csv filename
  TSTART                Integer of starting temperature value.
  TEND                  Integer of ending temperature value.
  NUMT                  Integer of amount of freeh values printed.
  INDEX_INT_LIST        (optional) Default printout is all freeh values. Read description below to filter freeh .csv results.

description of INDEX_INT_LIST:
  INDEX_INT_LIST if provided, .csv file output will be filtered.
  For example, if INDEX_INT_LIST = 0,17,6,13
    The csv file output will be filtered to only contain these output values:
      'T (K)' 'Total Energy freq (kJ/mol)' 'chem.pot. (kJ/mol)' 'enthalpy (kJ/mol)'
    Instead of containing all of the freeh results.
  freeh output value indexes:
     0='T (K)'
     1='P (MPa)'
     2='ln (qtrans)'
     3='ln (qrot)'
     4='ln(qvib)'
     5='chem.pot. (kJ/mol)'
     6='energy (kJ/mol)'
     7='entropy (kJ/mol/K)'
     8=''
     9='T (K)'
    10='P (MPa)'
    11='Cv (kJ/mol-K)'
    12='Cp (kJ/mol-K)'
    13='enthalpy (kJ/mol)'
    14=''
    15='T (K)'
    16='Total Energy freq (au)'
    17='Total Energy freq (kJ/mol)'
    18=''

options:
  -h, --help            show this help message and exit.

Written by Jeremy Schroeder 4-13-2024


```


### CSV_freeh.sh Example Output

``` title="CSV_thermo.csv Example Usage"
bash CSV_thermo.csv example_output.csv 250 500 6
```

<details>
<summary>example_output.csv File</summary>

```title="example_output.csv"
T (K),P (MPa),ln (qtrans),ln (qrot),ln(qvib),chem.pot. (kJ/mol),energy (kJ/mol),entropy (kJ/mol/K),,T (K),P (MPa),Cv (kJ/mol-K),Cp (kJ/mol-K),enthalpy (kJ/mol),,T (K),Total Energy freq (au),Total Energy freq (kJ/mol),
250.00,0.1000000,17.31,12.03,1.70,92.18,169.12,0.31610,,250.00,0.1000000,0.0827033,0.0910176,171.20,,250.00,-817.52609110919,-2146414.7522071786,
300.00,0.1000000,17.77,12.31,2.31,75.93,173.53,0.33366,,300.00,0.1000000,0.0934691,0.1017834,176.03,,300.00,-817.52609110919,-2146414.7522071786,
350.00,0.1000000,18.15,12.54,2.95,58.83,178.45,0.35008,,350.00,0.1000000,0.1030149,0.1113292,181.36,,350.00,-817.52609110919,-2146414.7522071786,
400.00,0.1000000,18.49,12.74,3.59,40.94,183.82,0.36552,,400.00,0.1000000,0.1115332,0.1198475,187.14,,400.00,-817.52609110919,-2146414.7522071786,
450.00,0.1000000,18.78,12.92,4.23,22.29,189.59,0.38008,,450.00,0.1000000,0.1191343,0.1274486,193.33,,450.00,-817.52609110919,-2146414.7522071786,
500.00,0.1000000,19.05,13.07,4.87,2.94,195.72,0.39387,,500.00,0.1000000,0.1259088,0.1342231,199.87,,500.00,-817.52609110919,-2146414.7522071786,


```
</details>

example_output.csv Table

| T (K) | P (MPa) | ln (qtrans) | ln (qrot) | ln(qvib) | chem.pot. (kJ/mol) | energy (kJ/mol) | entropy (kJ/mol/K) | T (K) | P (MPa) | Cv (kJ/mol-K) | Cp (kJ/mol-K) | enthalpy (kJ/mol) | T (K) | Total Energy freq (au) | Total Energy freq (kJ/mol) | 
| --- | --- |         --- |    --- |   --- |  --- |   --- |    --- |      --- |    --- |       --- |        --- |       --- |    --- |    --- |               --- |
| 250.00 | 0.1000000 | 17.31 | 12.03 | 1.70 | 92.18 | 169.12 | 0.31610 | 250.00 | 0.1000000 | 0.0827033 | 0.0910176 | 171.20 | 250.00 | -817.52609110919 | -2146414.7522071786 | 
| 300.00 | 0.1000000 | 17.77 | 12.31 | 2.31 | 75.93 | 173.53 | 0.33366 | 300.00 | 0.1000000 | 0.0934691 | 0.1017834 | 176.03 | 300.00 | -817.52609110919 | -2146414.7522071786 | 
| 350.00 | 0.1000000 | 18.15 | 12.54 | 2.95 | 58.83 | 178.45 | 0.35008 | 350.00 | 0.1000000 | 0.1030149 | 0.1113292 | 181.36 | 350.00 | -817.52609110919 | -2146414.7522071786 | 
| 400.00 | 0.1000000 | 18.49 | 12.74 | 3.59 | 40.94 | 183.82 | 0.36552 | 400.00 | 0.1000000 | 0.1115332 | 0.1198475 | 187.14 | 400.00 | -817.52609110919 | -2146414.7522071786 | 
| 450.00 | 0.1000000 | 18.78 | 12.92 | 4.23 | 22.29 | 189.59 | 0.38008 | 450.00 | 0.1000000 | 0.1191343 | 0.1274486 | 193.33 | 450.00 | -817.52609110919 | -2146414.7522071786 | 
| 500.00 | 0.1000000 | 19.05 | 13.07 | 4.87 | 2.94 | 195.72 | 0.39387 | 500.00 | 0.1000000 | 0.1259088 | 0.1342231 | 199.87 | 500.00 | -817.52609110919 | -2146414.7522071786 | 


