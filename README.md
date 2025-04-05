
Step 1: Build the Docker Image

- To build the Docker image, use the following command:
  docker build -t myapp .

Step 2: Verify the Docker Image

- To verify that the image was built successfully, use:
  docker images
  - This will show the list of images, and you should see `myapp` in the repository.

Step 3: Run the Docker Container

- To run the container, use the following command:
  docker run -d --name mycontainer myapp

Step 4: Verify Running Containers

- To check the running containers, use:
  docker ps

Step 5: Check Container Health

- To inspect the health status of the container, use:
  docker inspect <container_id_or_name>
  - Look for the "State.Health" section in the output.
  - The status should show `healthy` or `unhealthy` depending on the health check.

Step 6: Remove Running Containers

- If you want to remove the container, use:
  docker rm <container_id_or_name>

Step 7: Remove the Docker Image

- If you want to remove the image, use:
  docker rmi <image_id>
  - If the image is being used by a container, stop and remove the container first.
  - Example:
    docker stop <container_id_or_name>
    docker rm <container_id_or_name>
    docker rmi <image_id>

Step 8: Push the Image to Docker Hub

- To tag the image with your Docker Hub username:
  docker tag myapp:latest <username>/myapp:latest

- To push the image to Docker Hub, use:
  docker push <username>/myapp:latest

Step 9: Logout from Docker Hub

- Once done, you can log out of Docker Hub:
  docker logout
