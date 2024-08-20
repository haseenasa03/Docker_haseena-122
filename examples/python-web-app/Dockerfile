# Use an official Python runtime as a parent image
FROM python:3.9-slim

# Set environment variable to bypass the PEP 668 restriction
ENV PIP_BREAK_SYSTEM_PACKAGES=1

# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app/

# Install dependencies
RUN apt-get update && \
    apt-get install -y python3 python3-pip build-essential && \
    pip install --no-cache-dir -r requirements.txt

# Expose port 8000
EXPOSE 8000

# Command to run the application
CMD ["python", "manage.py", "runserver", "0.0.0.0:
