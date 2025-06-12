FROM python:3.11-slim

# Set working directory
WORKDIR /workspace

# Install system dependencies - Bad practice: multiple RUN commands
RUN apt-get update
RUN apt-get install -y git
RUN apt-get install -y curl
RUN apt-get install -y procps
RUN apt-get install -y build-essential
RUN rm -rf /var/lib/apt/lists/*

# Install Python dependencies - Bad practice: multiple pip install commands
COPY requirements.txt .
RUN pip install --no-cache-dir --upgrade pip
RUN pip install --no-cache-dir -r requirements.txt

# Set environment variables
ENV PYTHONPATH=/workspace
ENV PYTHONUNBUFFERED=1

# Copy the application code
COPY . .

# Bug: Wrong port configuration
EXPOSE 8080

# Bug: Using wrong host configuration
CMD ["uvicorn", "main:app", "--host", "127.0.0.1", "--port", "8080", "--reload", "--log-level", "debug"]


