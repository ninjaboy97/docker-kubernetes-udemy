Container lifecycle

docker run = docker create + docker start

You first have to create a container and can start it any number of times. "docker start" just runs the startup command on the container. 

NOTE: docker start -a <container-id> is needed to see the output from the container on the command line

New command: docker create <image> -- Used to create a container out of an imgae. Returns the container id which can be used to start the container later.

New command: docker start <container-id> -- Used to run a container referenced by container-id.

New command: docker system prune: Used to remove bulid cache and container history. It is a good idea to run this command everytime you're done working with docker for a while

New command: docker logs <container-id> -- Used to print the logs from the container. Can be used in case you forgot to specify the "-a" flag while running docker start.

New command: docker stop <container-id> -- Used to stop a container. Does a soft stop. Gives the process 10s to terminate. Sends a SIGTERM signal to the running process.

New command: docker kill <container-id> -- Instantly stops a running container. No time given to the process to gracefully terminate. Sends a SIGKILL signal to the running process.

Creating docker images


