# Define the base image
FROM python:3.10.2-slim
WORKDIR /app

# Update and upgrade the package list
RUN apt-get update -y \
  && apt-get upgrade -y \
  && rm -rf /var/lib/apt/lists/*

COPY project/requirements.txt

# Install Django and its dependencies
RUN pip install django

# Create a working directory for the Django project


# Copy the Django project files to the container
COPY . /app

# Run the Django development server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]
