
# Common Docker Commands

This repository is a small collection of commonly used Docker commands, designed to help beginners get started with Docker and containerization. Docker is a platform that allows you to develop, ship, and run applications inside lightweight, portable containers. Containers provide a consistent environment for your applications, making it easier to manage dependencies and run your software reliably across different environments.

## Docker Commands

1. **To pull and run an image:**
   ```sh
   docker run imagename
   ```
   This command pulls the specified image from Docker Hub (if not already available locally) and runs it.

2. **To pull an image:**
   ```sh
   docker pull imagename
   ```
   This command pulls the specified image from Docker Hub to your local machine.

3. **To list all running containers:**
   ```sh
   docker ps
   ```
   This command lists all currently running containers.

4. **To list all containers (running and stopped):**
   ```sh
   docker ps -a
   ```
   This command lists all containers, including those that are stopped.

5. **To start a stopped container:**
   ```sh
   docker start container_id
   ```
   This command starts a container that was previously stopped.

6. **To stop a running container:**
   ```sh
   docker stop container_id
   ```
   This command stops a running container.

7. **To remove a container:**
   ```sh
   docker rm container_id
   ```
   This command removes a container. Note that the container must be stopped before it can be removed.

8. **To remove an image:**
   ```sh
   docker rmi imagename
   ```
   This command removes an image from your local machine.

9. **To execute a command in a running container:**
   ```sh
   docker exec -it container_id command
   ```
   This command runs a specified command inside a running container. The `-it` flags allow for interactive terminal access.

10. **To build an image from a Dockerfile:**
    ```sh
    docker build -t imagename:tag .
    ```
    This command builds a Docker image from a Dockerfile in the current directory. The `-t` flag tags the image with a name and optionally a version tag.

11. **To see the logs of a container:**
    ```sh
    docker logs container_id
    ```
    This command shows the logs of a specified container.

12. **To inspect a container:**
    ```sh
    docker inspect container_id
    ```
    This command provides detailed information about a specified container.

13. **To remove all stopped containers:**
    ```sh
    docker container prune
    ```
    This command removes all stopped containers.

14. **To remove all unused images:**
    ```sh
    docker image prune -a
    ```
    This command removes all unused images (those not used by any container).

15. **To tag an image:**
    ```sh
    docker tag source_image:tag target_image:tag
    ```
    This command tags an image with a new name and/or tag.

16. **To push an image to Docker Hub:**
    ```sh
    docker push imagename:tag
    ```
    This command pushes a tagged image to Docker Hub.

## Advance run commands

1. **To run a container in detached mode:**
   ```sh
   docker run -d imagename
   ```
   This command runs the container in the background and prints the container ID.

2. **To run a container with port binding:**
   ```sh
   docker run -p host_port:container_port imagename
   ```
   This command maps a port on the host to a port on the container.

3. **To run a container with a specific name:**
   ```sh
   docker run --name container_name imagename
   ```
   This command runs the container with a specific name.

4. **To run a container with an environment variable:**
   ```sh
   docker run -e "ENV_VAR_NAME=value" imagename
   ```
   This command sets an environment variable in the container.

5. **To run a container with a volume:**
   ```sh
   docker run -v host_directory:container_directory imagename
   ```
   This command mounts a directory from the host into the container.

6. **To run a container interactively:**
   ```sh
   docker run -it imagename
   ```
   This command runs the container in interactive mode with a terminal.

7. **To remove a container automatically after it exits:**
   ```sh
   docker run --rm imagename
   ```
   This command removes the container once it exits.

8. **To limit a container's memory usage:**
   ```sh
   docker run -m memory_limit imagename
   ```
   This command limits the amount of memory the container can use.

9. **To run a container with a custom network:**
   ```sh
   docker run --network network_name imagename
   ```
   This command connects the container to a custom network.

## Docker Compose Commands

1. **To start services defined in a `docker-compose.yml` file:**
   ```sh
   docker-compose up
   ```
   This command starts all services defined in the `docker-compose.yml` file. Use the `-d` flag to run them in detached mode.

2. **To stop services defined in a `docker-compose.yml` file:**
   ```sh
   docker-compose down
   ```
   This command stops and removes all services defined in the `docker-compose.yml` file.

3. **To build images defined in a `docker-compose.yml` file:**
   ```sh
   docker-compose build
   ```
   This command builds all images defined in the `docker-compose.yml` file.

4. **To see the logs of services defined in a `docker-compose.yml` file:**
   ```sh
   docker-compose logs
   ```
   This command shows the logs of all services defined in the `docker-compose.yml` file.

---

Feel free to add more commands by creating a PR (Pull Request) that can be helpful for others!
