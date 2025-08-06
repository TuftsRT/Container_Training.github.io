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
