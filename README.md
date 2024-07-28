
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
