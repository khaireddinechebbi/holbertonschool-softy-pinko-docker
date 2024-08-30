# Use the latest version of Ubuntu as the base image
FROM ubuntu:latest

# Update the package list and upgrade the installed packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove EXTERNALLY-MANAGED file if present
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask using pip3
RUN pip3 install flask

# Set the working directory to /app
WORKDIR /app

# Copy the api.py file into the Docker image
COPY ./api.py /app/api.py

# Expose port 5252 to the host
EXPOSE 5252

# Run the Flask app
CMD ["python3", "api.py"]
