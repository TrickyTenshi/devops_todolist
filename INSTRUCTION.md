ToDo App Docker Instructions

1. Docker Hub Repository
The pre-built image is available at the following link:
https://hub.docker.com/r/trickykot3/todoapp

2. Build Instructions
To build the image locally, run the following command in the root directory of the project:

docker build -t trickykot3/todoapp:1.0.0 .

Changing the Python version:
You can specify a different base Python version using a build argument.
(Warning: Changing the version may cause some features to work incorrectly or break the application. The default version is set to 3.11).

docker build --build-arg PYTHON_VERSION=<python_version> -t trickykot3/todoapp:1.0.0 .

3. Run Instructions
To start the container and map the required ports, use the following command:

docker run -p 8080:8080 --name <your_container_name> trickykot3/todoapp:1.0.0

Running in detached (background) mode:
If you want to run the container in the background, add the -d flag:

docker run -d -p 8080:8080 --name <your_container_name> trickykot3/todoapp:1.0.0

4. Accessing the Application
Once the container is up and running, you can access the application via your web browser at:
http://localhost:8080