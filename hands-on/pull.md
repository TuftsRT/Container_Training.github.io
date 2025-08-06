## singularity/apptainer pull

### Syntax

Download or build a container from a given URI.

```
$ singularity/apptainer pull [output file] <URI>
```

### Example

To pull the blast image from [Docker hub](https://hub.docker.com/r/ncbi/blast/tags), you can simply use the following command.

```
singularity pull docker://ncbi/blast:2.17.0
```
