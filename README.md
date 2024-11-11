# PythonProject

**PythonProject** is a simple web application built using Flask that serves a "Hello World" message from a Python file. This project is dockerized to make it easy to deploy and run in any environment.

## Project Structure

The basic structure of the project is as follows:

```
PythonProject/
│
├── app.py            # Python file that contains the Flask application
├── Dockerfile        # Dockerfile to build the container image
└── README.md         # Project documentation
```

### Requirements

To run this project locally or inside a Docker container, you need the following:

1. **Docker** (if you want to run in a container)
2. **Git** (to clone the repository)

### Local Installation and Execution

#### 1. Clone the Repository

Clone it using Git:

```bash
git clone https://github.com/lessalcu/PythonProject.git
cd PythonProject
```

#### 2. Build the Docker Image

To build the Docker image, run the following command:

```bash
docker build -t lssalas/python-project .
```

#### 3. Run the Application

Once the image is built, run the container:

```bash
docker run -d -p 5000:5000 lssalas/python-project
```

The application will be available at `http://localhost:5000/` and you should see the message **¡Hello world from Python, Lesly Salas SI08!**.

**Note:** If you encounter an error with port `5000` being already in use, you can either:
- Terminate the process occupying the port (use `taskkill /PID <PID> /F` for Windows to stop the process), or
- Run the container on a different port, such as `5001`, by using the command `docker run -d -p 5001:5000 lssalas/python-project`.

### Docker Hub Launch Manual

#### 1. Download the Image

To download the image from Docker Hub, run:

```bash
docker pull lssalas/python-project:latest
```

#### 2. Run the Container

Once the image is downloaded, run the container:

```bash
docker run -d -p 5000:5000 lssalas/python-project:latest
```

This will start the container and the application will be available at `http://localhost:5000/`.

## Notes

- Make sure Docker is running.
- If you have problems accessing `http://localhost:5000`, verify that the port is not in use or check your firewall.

## Credits

- Project developed by **Lesly Salas** (https://github.com/lessalcu).