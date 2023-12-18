# Create a file named Dockerfile in the root of your Django project.
# This file contains instructions for building a docker image for your app
# We are using officila python runtime as a parent image
FROM python:3.8

# We are setting the working directory in the container
WORKDIR /app

# We are copying whole local directory files to the container
COPY . /app

#Install any needed packages specified in requirements.txt
RUN pip install --no-cache-dir -r requirements.txt

#Make port 8000 available to the world outside the container
EXPOSE 8000

# Defining the environment variable
ENV Name World

# Run app.py when the container launches
CMD ["python","manage.py","runserver","0.0.0.0:8000"]