# Django REST Framework Backend Dockerfile
FROM python:3.11-slim

# Install system dependencies for PostgreSQL and building Python packages
RUN apt-get update \
    && apt-get install -y --no-install-recommends \
        postgresql-client \
        build-essential \
        libpq-dev \
    && rm -rf /var/lib/apt/lists/*

# Set environment variables
ENV PYTHONDONTWRITEBYTECODE=1
ENV PYTHONUNBUFFERED=1

# Set work directory
WORKDIR /app

# Install Python dependencies
COPY requirements.txt /app/
RUN pip install --no-cache-dir -r requirements.txt

# Copy project
COPY . /app/

# Create directories for static files and media
RUN mkdir -p /app/staticfiles /app/media

# Expose port
EXPOSE 8000

# Run the application with migrations
CMD python manage.py migrate && python manage.py runserver 0.0.0.0:8000
