# FastAPI Technical Test

## Exercise Description

This technical test is designed to evaluate your understanding of basic infrastructure concepts, containerisation, and programming practices. The project contains several intentionally introduced bugs and suboptimal configurations that you need to identify and fix.

### Tasks

1. Identify and fix the Docker configuration issues:
   - Analyse the Dockerfile for inefficient practices
   - Correct the container networking configuration
   - Ensure the application runs properly in a containerised environment

2. Debug the FastAPI application:
   - Locate and fix three code-level bugs
   - Implement proper error handling
   - Ensure database operations work correctly

3. Document your solutions:
   - Explain each issue you found
   - Provide the corrected code
   - Justify your changes

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

### Docker Development

1. Build the Docker image:
```bash
docker build -t fastapi-test .
```

2. Run the container:
```bash
docker run -p 8000:8000 fastapi-test
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

## Evaluation Criteria

Your solution will be evaluated based on:
- Correct identification of all issues
- Quality of the fixes implemented
- Understanding of containerisation concepts
- Code quality and best practices
- Documentation clarity