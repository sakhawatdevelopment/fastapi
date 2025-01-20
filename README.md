# FastAPI Hello World

This is a simple FastAPI application that returns "Hello, World!" as a JSON response. The app is containerized using Docker and Docker Compose for easy setup and deployment.

## Prerequisites

- [Docker](https://www.docker.com/get-started)
- [Docker Compose](https://docs.docker.com/compose/install/) (typically comes with Docker)

## Project Structure

```
fastapi-hello-world/
├── Dockerfile
├── docker-compose.yml
├── main.py
├── requirements.txt
└── README.md
```

- `Dockerfile`: Contains instructions to build the Docker image for the FastAPI app.
- `docker-compose.yml`: Defines the services and configurations for Docker Compose.
- `main.py`: FastAPI app that serves a "Hello, World!" response.
- `requirements.txt`: Lists the Python dependencies.

## Setup and Run

### 1. Clone the repository

If you haven't already, clone the repository to your local machine:

```bash
git clone https://github.com/sakhawatdevelopment/fastapi.git
cd fastapi
```

### 2. Build and start the app with Docker Compose

Run the following command to build the image and start the app:

```bash
docker-compose up --build
```

Docker Compose will build the image based on the `Dockerfile` and start the FastAPI app in a container.

### 3. Access the app

Once the app is running, open your browser and navigate to:

```
http://localhost:8000
```

You should see a response like:

```json
{"message": "Hello, World!"}
```

### 4. Explore the interactive API documentation

FastAPI automatically generates interactive API documentation:

- Swagger UI: [http://localhost:8000/docs](http://localhost:8000/docs)
- ReDoc: [http://localhost:8000/redoc](http://localhost:8000/redoc)

### 5. Stop the app

To stop the app, use:

```bash
docker-compose down
```

This will stop and remove the running containers.