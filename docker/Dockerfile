# Use an official Python runtime as a parent image
FROM python:3.10-slim@sha256:31dd4d9529d02d7436659061cb7564cd4733fc90e5e152709a942d53382ec8d0

# Set the working directory in the container
WORKDIR /app

# Install dependencies
COPY requirements.txt .
RUN pip install --no-cache-dir -r requirements.txt

# Copy application code
COPY app.py .

# Run the application
# Make port 80 available to the world outside this container
EXPOSE 80

ENV NAME World

# Run the application
CMD ["python", "app.py"]
