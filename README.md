# Tufts TTS RT Internal training: Workflow for Building, Managing, and Running Containers

Containers have become a transformative technology in HPC, offering significant advantages in portability, reproducibility, performance, isolation, and security. They are rapidly gaining adoption in scientific computing and are poised to play a pivotal role in the future of HPC.

In this training, you’ll learn the workflow Tufts RT used
Topics include:

- What are containers and why should we use them
- How to use Singularity/Apptainer to pull and run containers
- How to build containers with Docker and Apptainer
- Environment modules (ngc and biocontainers) based on containers
- Advanced topics namely multinode-MPI and GPU containers
- Hands-on Demo

## Take home messages

- To ensure that you're not wasting your time building your own containers, it's recommended to check if there are any publicly available containers that can serve your purpose.
- If you plan to use GPU containers, ensure compatibility between the CUDA version that was used to build the target application inside container and our GPU’s CUDA driver version.
- When running containers that require GPU, make sure to include the `--nv` flag.
- Remember to use `ncdu`, a helpful tool, to regularly check and clean up `$HOME/.apptainer` and `$HOME/.singularity` directories.
