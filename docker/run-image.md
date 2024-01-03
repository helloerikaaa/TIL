# Docker Run Command

The docker run command is fundamental in the operationalization of Docker containers, enabling the deployment and execution of Docker images. The general syntax for this command is exemplified as follows:

```bash
docker run -d -p <port:port> <image-name>
```
- `-d (detach)`: This flag runs the Docker container in the background, freeing the terminal for other commands. It decouples the container's lifecycle from the terminal session, allowing it to persist independently.

- `-p port:port`: This flag is pivotal for mapping the ports between the host system and the container. The `<port:port>` parameter signifies the mapping of ports, where the left side represents the host port, and the right side represents the container port. This is crucial for facilitating communication with services within the container.

- `<image-name>`: This parameter specifies the Docker image to be instantiated as a container. It should correspond to the name of the previously built Docker image.