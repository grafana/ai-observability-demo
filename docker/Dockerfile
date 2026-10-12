# Use an official Python runtime as a parent image
FROM python:3.14-slim@sha256:a2b82f3c48559aa0a8446d9af49826b6e2b2016f4cd2afabfe6013ec53729170

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
