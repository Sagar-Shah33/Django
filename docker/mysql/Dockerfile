# Define the base image
FROM mysql:latest

# Set environment variables for the database
ENV MYSQL_ROOT_PASSWORD password

# Create the database
RUN mysql -u root -p"$MYSQL_ROOT_PASSWORD" << EOF
CREATE DATABASE project;
CREATE USER 'rohit'@'%' IDENTIFIED BY 'sagar';
GRANT ALL PRIVILEGES ON project.* TO 'rohit'@'%';
EOF

# Expose the database port
EXPOSE 3306
