# Installing Redis Using Docker
    docker pull redis

# Run the Redis container with the following command:
    docker run -d -p 6379:6379 --name redis-cache redis

# Here
	•	-d: Runs the container in detached mode (in the background).
	•	-p 6379:6379: Maps port 6379 on your machine to port 6379 in the container, allowing the Spring Boot application to access Redis on the default port.
	•	--name redis-cache: Assigns a name to the container for easier management.

# Verify that Redis is running:
    docker ps

# Login to Redis CLI:
    docker exec -it redis-cache redis-cli

# Commands:
    ping (it will respond PONG)
    KEYS * (it will show all the cached keys)
