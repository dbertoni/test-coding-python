# FastAPI Test Project

This is a simple FastAPI project with SQLite integration, designed to run in GitHub Codespaces.

## Features

- FastAPI REST API
- SQLite database with SQLAlchemy ORM
- GitHub Codespaces configuration
- Basic CRUD operations for items

## Getting Started

### Local Development

1. Create a virtual environment:
```bash
python -m venv venv
source venv/bin/activate  # On Windows: venv\Scripts\activate
```

2. Install dependencies:
```bash
pip install -r requirements.txt
```

3. Run the application:
```bash
uvicorn main:app --reload
```

The API will be available at http://localhost:8000

### GitHub Codespaces

1. Open this repository in GitHub Codespaces
2. The development container will automatically set up the environment
3. Run the application:
```bash
uvicorn main:app --host 0.0.0.0 --port 8000
```

## API Documentation

Once the application is running, you can access:
- Interactive API documentation: http://localhost:8000/docs
- Alternative API documentation: http://localhost:8000/redoc

## API Endpoints

- `GET /`: Welcome message
- `POST /items/`: Create a new item
- `GET /items/`: List all items
- `GET /items/{item_id}`: Get a specific item