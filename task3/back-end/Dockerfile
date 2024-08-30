# Use the latest version of Ubuntu as the base image
FROM ubuntu:latest

# Update the package list and upgrade all packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# If needed, remove the EXTERNALLY-MANAGED file to allow pip installations
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED

# Install Flask and Flask-CORS using pip3
RUN pip3 install flask flask-cors

# Set the working directory inside the Docker container
WORKDIR /app

# Copy the Flask app file to the Docker image
COPY ./api.py /app/api.py

# Set the command to run the Flask server
CMD ["python3", "api.py"]
