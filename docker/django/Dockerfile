# Define the base image
FROM python:3.10.2-slim
WORKDIR /app

# Update and upgrade the package list
RUN apt-get update -y \
  && apt-get upgrade -y \
  && apt-get install libmysqlclient-dev default-libmysqlclient-dev -y \
  && rm -rf /var/lib/apt/lists/*

COPY project/requirements.txt

# Install Django and its dependencies
RUN pip install mysqlclient
RUN pip install -r requirements.txt

# Create a working directory for the Django project


# Copy the Django project files to the container
COPY Django/ /app

# Run the Django development server
CMD ["cd projects && python manage.py runserver 0.0.0.0:8000"]
