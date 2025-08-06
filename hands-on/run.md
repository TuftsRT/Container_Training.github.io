# singularity exec

Singularity has a `run` subcommand. This can be used to run the user-defined default command within a container. However, it is recommended to use another subcommand `exec` instead of `run`. If you're interested in `run`, please check the [singularity user guide](https://docs.sylabs.io/guides/3.8/user-guide/cli/singularity_run.html#singularity-run).

## Syntax

Download or build a container from a given URI.

```
singularity exec [options] image command
```

## Example

### Blast

```
$ singularity exec blast_2.17.0.sif makeblastdb -in blastdb.faa -dbtype prot -out blastdb
```

### Pytorch

```
$ singularity exec pytorch_2.1.2-cuda11.8-cudnn8-runtime.sif python torch_demo.py
```
