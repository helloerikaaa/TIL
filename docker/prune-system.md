# Docker System Prune Command

The docker system prune command is a powerful tool for reclaiming disk space by removing unused resources in a Docker environment. The `-a` flag is added to remove all images, not just dangling ones. The basic syntax for this command is as follows:

```bash
docker system prune -a
```

- `-a`: This flag extends the pruning operation to include all images, regardless of whether they are currently in use. It effectively cleans the system of all unused Docker resources.


This command is particularly relevant for maintaining a lean and efficient Docker environment by removing obsolete images, containers, volumes, and networks that are no longer needed.