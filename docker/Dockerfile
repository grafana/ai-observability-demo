# Use an official Python runtime as a parent image
FROM python:3.9-slim@sha256:2d97f6910b16bd338d3060f261f53f144965f755599aab1acda1e13cf1731b1b

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
