## Docker Installation

### Configure the Docker Repository

*Source: <https://github.com/NicolasW-7/AIS-Brief-et-TIPS/blob/main/Procedure/Docker/Installation%20Docker.md?plain=1>*

1. Update the package list:

    ```sh
    sudo apt-get update
    ```

2. Install the necessary packages:

    ```sh
    sudo apt-get install ca-certificates curl gnupg
    ```

3. Create the directory for the repository keys:

    ```sh
    sudo install -m 0755 -d /etc/apt/keyrings
    ```

4. Download and add the Docker GPG key:

    ```sh
   curl -fsSL https://download.docker.com/linux/debian/gpg | sudo gpg --dearmor -o /etc/apt/keyrings/docker.gpg
    ```

5. Change the permissions of the GPG key:

    ```sh
    sudo chmod a+r /etc/apt/keyrings/docker.gpg
    ```

6. Add the Docker repository to the APT sources list:

    ```sh
    echo "deb [arch=$(dpkg --print-architecture) signed-by=/etc/apt/keyrings/docker.gpg] https://download.docker.com/linux/debian $(lsb_release -cs) stable" | sudo tee /etc/apt/sources.list.d/docker.list > /dev/null
    ```

7. Update the package list to include the Docker repository:

    ```sh
    sudo apt-get update
    ```

8. Install the necessary Docker packages:

    ```sh
    sudo apt-get install docker-ce docker-ce-cli containerd.io docker-buildx-plugin docker-compose-plugin
      ```

### Verify Docker Installation

9. Check the status of the Docker service:

    ```sh
    systemctl status docker
    ```

10. If Docker is "active (running)", enable the Docker service to start automatically after the machine reboots:

    ```sh
    sudo systemctl enable docker
    ```

### Useful Docker Commands

- `docker ps -a`: Shows all containers, including their status, creation date, age, name, and ID.
- `docker stop <container_id>` / `docker rm <container_id>`: Stops (`stop`) and removes (`rm`) a container by adding its ID.
- `docker compose up -d`: Runs the `docker-compose.yml` file to start the containers in detached mode (`-d`).

#### Command Details

##### `docker ps -a`

Displays all containers, whether running or stopped, with information such as:

- Container ID
- Image used
- Command executed
- Creation date
- Status (running, stopped, etc.)
- Exposed ports
- Container names

##### `docker stop <container_id>` / `docker rm <container_id>`

- `docker stop <container_id>`: Stops a running container.
- `docker rm <container_id>`: Removes a stopped container.

**Example:**

```sh
docker stop 1a2b3c4d5e6f
docker rm 1a2b3c4d5e6f
```
