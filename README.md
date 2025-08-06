Containers have become a transformative technology in HPC, offering significant advantages in portability, reproducibility, performance, isolation, and security. They are rapidly gaining adoption in scientific computing and are poised to play a pivotal role in the future of HPC.

In this training, you’ll learn the workflow Tufts RT used to build, manage, pull and run containers on Tufts HPC.

Topics include:

- What are containers and why should we use them?
- Container registry - Docker Hub.
- How to use GitHub action to build docker containers?
- How to use singularity/apptainer to pull containers?
- How to use `container-mod` to pull containers, generate modules, and jupyter kernels?
- How to build containers using your personal computers?

## Take home messages

- To ensure that you're not wasting your time building your own containers, it's recommended to check if there are any publicly available containers that can serve your purpose.
- If you plan to use GPU containers, ensure compatibility between the CUDA version that was used to build the target application inside container and our GPU’s CUDA driver version.
- When running containers that require GPU, make sure to include the `--nv` flag.
- Remember to use `ncdu`, a helpful tool, to regularly check and clean up `$HOME/.apptainer` and `$HOME/.singularity` directories.

## Hands-on

- [Load modules](hands-on/load_modules.md)
- [singularity pull](hands-on/pull.md)
- [singularity shell](hands-on/shell.md)
- [singularity run](hands-on/run.md)
- [docker build](hands-on/build.md)
- [github action](hands-on/github_action.md)
- [container-mod](hands-on/container-mod.md)

## Recommended base images

## Recommended base images

| Usage                    | Name              | Link                                                                                             |
| ------------------------ | ----------------- | ------------------------------------------------------------------------------------------------ |
| Operation system         | ubuntu            | [https://hub.docker.com/\_/ubuntu](https://hub.docker.com/_/ubuntu)                              |
| Operation system         | rockylinux        | [https://hub.docker.com/\_/rockylinux](https://hub.docker.com/_/rockylinux)                      |
| Python                   | python            | [https://hub.docker.com/\_/python](https://hub.docker.com/_/python)                              |
| R/Rstudio                | rocker/tidyverse  | [https://hub.docker.com/r/rocker/tidyverse](https://hub.docker.com/r/rocker/tidyverse)           |
| R/Rstudio                | rocker/geospatial | [https://hub.docker.com/r/rocker/geospatial](https://hub.docker.com/r/rocker/geospatial)         |
| R/Rstudio                | rocker/cuda       | [https://hub.docker.com/r/rocker/cuda](https://hub.docker.com/r/rocker/cuda)                     |
| R/Rstudio                | rocker/ml         | [https://hub.docker.com/r/rocker/ml](https://hub.docker.com/r/rocker/ml)                         |
| GPU                      | nvidia/cuda       | [https://hub.docker.com/r/nvidia/cuda](https://hub.docker.com/r/nvidia/cuda)                     |
| Data Science             | pytorch           | [https://hub.docker.com/r/pytorch/pytorch](https://hub.docker.com/r/pytorch/pytorch)             |
| Data Science             | tensorflow        | [https://hub.docker.com/r/tensorflow/tensorflow](https://hub.docker.com/r/tensorflow/tensorflow) |
| Our organization account | tuftsttsrt        | [https://hub.docker.com/u/tuftsttsrt](https://hub.docker.com/u/tuftsttsrt)                       |
