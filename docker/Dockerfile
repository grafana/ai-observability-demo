# Use an official Python runtime as a parent image
FROM python:3.13-slim@sha256:dc1546eefcbe8caaa1f004f16ab76b204b5e1dbd58ff81b899f21cd40541232f

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
