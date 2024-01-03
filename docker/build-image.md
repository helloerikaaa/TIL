# Docker Build Command

The docker build command is an essential component in containerization, allowing the creation of Docker images from a set of instructions defined in a Dockerfile. The general syntax for this command is as follows:

```bash
docker build -t <image-name> .
```
- `-t <image-name>`: This flag is used to specify the desired name and optionally a tag for the Docker image. The `<image-name>` parameter serves as a user-defined label for the image.

- `. (dot)`: The period at the end signifies the build context. It specifies the location of the Dockerfile and other necessary files required for building the image. The build context includes all files and subdirectories in the specified location.