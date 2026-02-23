# Backend Project

A Python-based backend service containerized using Docker and orchestrated with Docker Compose. This project is designed to provide a scalable and portable backend environment suitable for development and deployment.

---

##  Features

* Python backend application
* Dockerized for consistent environments
* Docker Compose support for multi-service setup
* Database migrations support
* Logging and file upload handling
* Modular project structure

---

## Project Structure

```
backend-project/
│
├── app/                    # Application source code
├── migrations/             # Database migration files
├── uploads/                # Uploaded files (ignored in git)
├── logs/                   # Log files (ignored in git)
├── backups/                # Backup files
├── main.py                 # Application entry point
├── requirements.txt        # Python dependencies
├── Dockerfile              # Docker image configuration
├── docker-compose.yml      # Multi-container orchestration
└── alembic.ini             # Alembic configuration
```

---

##  Running with Docker

### Build the Docker image

```bash
docker build -t backend-app .
```

###  Run the container

```bash
docker run -p 8000:8000 backend-app
```

The backend service will be available at:

```
http://localhost:8000
```

---

## Running with Docker Compose (Recommended)

### Start services

```bash
docker compose up --build
```

### Run in detached mode

```bash
docker compose up -d --build
```

### Stop services

```bash
docker compose down
```

---

## Installing Dependencies Locally (Optional)

If you want to run without Docker:

```bash
pip install -r requirements.txt
python main.py
```

---

## Environment Configuration

If your project uses environment variables, create a `.env` file in the root directory and configure required values.

Example:

```
PORT=8000
DEBUG=True
```

---

## Running Tests

```bash
pytest
```

(Ensure pytest is included in requirements.)

---

##  Notes

* Ensure Docker is installed and running.
* The `uploads/` and `logs/` folders are excluded from version control.
* Update the port mappings if your application uses a different port.

---

## Author

**Nikhil Ranasubhe**

---

## License

This project is for learning and development purposes.
