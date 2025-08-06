## Dockerfile

A Dockerfile is a plain-text file containing instructions that tell Docker how to build an image.
Think of it as a recipe: - You start from a base image - You install software or copy files into it - You define how the container should run

### FROM

We can use the `FROM` instruction to start our new image from a known base image.
This should be the first line of our Dockerfile.

```
FROM ubuntu:24.04
```

Base images typically take the form `os:version`. Avoid using the `latest` version; it is hard to track where it came from and the identity of `latest` can change.

### RUN

We can install updates, install new software, or download code to our image by running commands with the `RUN` instruction.

```
RUN apt-get update
RUN apt-get upgrade -y
RUN apt-get install -y python3
```

Each `RUN` instruction creates an intermediate image (called a `layer`). Too many layers makes the Docker image less performant, and makes building less efficient. We can minimize the number of layers by combining the RUN instructions:

```
RUN apt-get update && apt-get upgrade -y && apt-get install -y python3
```

### COPY

There are a couple different ways to get your source code inside the image. One way is to use a `RUN` instruction with `wget` to pull your code from the web. When you are developing, however, it is usually more practical to copy code in from the Docker build context using the `COPY` instruction.

```
COPY qe-7.4.1-ReleasePack.tar /opt/qe-7.4.1-ReleasePack.tar
```

### ENV

Another useful instruction is the `ENV` instruction. This allows the image developer to set environment variables inside the container runtime. For example, we usually need to set `PATH` or `LD_LIBRARY_PATH`.

### WORKDIR

The `WORKDIR` instruction in a Dockerfile sets the current working directory for any subsequent instructions like `RUN` and `COPY`.

### Example

```
# Step 1: Base image
FROM python:3.11-slim

# Step 2: Set working directory
WORKDIR /app

# Step 3: Copy files into the image
COPY requirements.txt .
COPY app.py .

# Step 4: Install dependencies
RUN pip install --no-cache-dir -r requirements.txt

# Step 5: Run the app
CMD ["python", "app.py"]
```

- [singularity run](hands-on/github_action.md)
