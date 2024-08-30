# latest Ubuntu image as the base
FROM ubuntu:latest

# Update APT package lists and upgrade installed packages
RUN apt-get update && apt-get upgrade -y

# Install Python3 and pip3
RUN apt-get install -y python3 python3-pip

# Remove the externally managed environment restriction, if needed
RUN rm /usr/lib/python*/EXTERNALLY-MANAGED || true

# Install Flask using pip3
RUN pip3 install Flask

# Set the working directory
WORKDIR /app

# Copy the Flask app into the Docker image
COPY api.py /app

# Expose port 5252 to the outside world
EXPOSE 5252

# Command to run the Flask app
CMD ["python3", "api.py"]
