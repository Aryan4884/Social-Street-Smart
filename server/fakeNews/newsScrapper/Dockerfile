#Use an official Python runtime as a parent image
FROM python:3.10-slim

RUN pip install --upgrade pip
# Set the working directory in the container
WORKDIR /app

# Copy the current directory contents into the container at /app
COPY . /app

# Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

ENV AWS_DEFAULT_REGION=us-east-1

# Expose the port the app runs on
EXPOSE 5000

# Define environment variable for Flask
ENV FLASK_APP=app.py
ENV FLASK_ENV=production

# Run the application
CMD ["python", "app.py", "--host=0.0.0.0"]
