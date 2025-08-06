## Start an interactive job

```
$ srun -N1 -n2 -t2:00:00 --pty bash ## You will start an interactive session
```

## Old cluster

### Singularity

```
$ module load singularity/3.8.4
$ module list
  1) squashfs/4.4                 2) singularity/3.8.4(default)
```

## New cluster

### Singularity

```
$ module load singularity/4.3.1
```

## Apptainer

```
$ module load apptainer/1.4.0
```

[Next: Singularity pull](pull.md)
