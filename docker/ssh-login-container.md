# Docker Exec Command

The docker exec command facilitates interactive execution within a running Docker container, enabling direct access to its command-line interface. The general syntax for this command is exemplified as follows:

```bash
docker exec -it <container-name> /bin/bash
```

- `-it`: This flag combines the options `-i (interactive)` and `-t (pseudo-TTY)`, allowing the user to interact with the container's command-line interface.

- `<container-name>`: Specifies the name or ID of the target Docker container where the interactive session will be initiated.

- `/bin/bash`: Indicates the command to be executed within the container, in this case, starting an interactive Bash shell.