# Use an official Python runtime as a parent image
FROM python:3.14-slim@sha256:ce40764625a4ff50df3548277632e7f96c4e77fe75fa848aae9885476e7df5a4

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
