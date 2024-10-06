# Gee-Python

This guide will walk you through running a Docker container using the provided Dockerfile, setting up the Conda environment, and executing the `gee-analysis.ipynb`

## Prerequisites

Ensure that you have the following installed on your machine:

- [Docker](https://docs.docker.com/get-docker/)
- Clone of this repository

## Steps to Run the Docker Container

### 1. Build the Docker Image

First, navigate to the `gee-python` directory where your `Dockerfile` is located. Run the following command to build the Docker image:

```bash
docker build -t gee-image .
```

### 2. Run the Docker Container

Once the image has been successfully built, run the container using the following command:

```bash
docker run -p 8888:8888 -v $(pwd):/home/jupyteruser --name gee-container gee-image
```

### 3. Access JupyterLab

Once the container is running, JupyterLab will start and an access token will be printed in the terminal.

### 4. Open the Notebook

After logging into JupyterLab, you should see the gee-analysis.ipynb notebook in the directory. Click to open it, and you can start running the code.
