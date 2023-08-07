# Docker React Commands Readme

This readme provides an explanation of each command used in the Docker commands to build and run an React application using Docker containers. The provided commands assume you have Docker installed on your system.

### 1. Build Docker Image: `docker build -t react-docker-image .`

- `docker build`: This command is used to build a Docker image from a Dockerfile.
- `-t react-docker-image`: The `-t` flag is used to tag the built image with a name, in this case, "react-docker-image". The name can be chosen by the user.
- `.`: The dot (`.`) at the end of the command specifies the build context. It tells Docker to use the current directory (where the Dockerfile is located) as the build context.

### 2. Run Docker Container: `docker run --rm --name react-docker-container -e WATCHPACK_POLLING=true -d -p 3000:3000 -v "path-to-the-folder:/app" react-docker-image`

- `docker run`: This command is used to create and start a new container from a Docker image.
- `--rm`: The `--rm` flag indicates that the container should be automatically removed when it exits (stops running).
- `--name react-docker-container`: The `--name` flag is used to provide a custom name for the container, in this case, "react-docker-container".
- `-e WATCHPACK_POLLING=true`: The `-e` flag is used to set environment variables within the container. In this case, it sets an environment variable `WATCHPACK_POLLING` to `true`.
- `-d`: The `-d` flag stands for "detached" mode. It runs the container in the background, and the terminal remains available for other commands.
- `-p 3000:3000`: The `-p` flag maps the host port to the container port. In this case, it maps port 3000 from the host to port 3000 in the container, allowing access to the web application running inside the container.
- `-v "path-to-the-folder:/app`": The `-v` flag is used to mount a volume. It allows the specified directory on the host (`path-to-the-folder`) to be mounted inside the container at the `/app` directory. This is useful for development, as it enables live code changes without rebuilding the image.
- `react-docker-image`: This is the name of the Docker image to run the container from.

### 3. List Running Containers: `docker ps`

- `docker ps`: This command is used to list the currently running containers.

### 4. View Container Logs: `docker logs react-docker-container`

- `docker logs`: This command is used to view the logs of a specific container.
- `react-docker-container`: This is the name of the container for which we want to view the logs.

### 5. Stop Running Container: `docker stop react-docker-container`

- `docker stop`: This command is used to stop a running container gracefully.
- `react-docker-container`: This is the name of the container to stop.

With this information, you should have a better understanding of the Docker commands and how to run an React application inside a Docker container. Happy coding!
