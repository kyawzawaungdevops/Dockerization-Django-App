FROM python:3.9

#Install Django and other required packages
RUN pip install django

# Copy the Django project files into the image
COPY . /app

# Set the working directory
WORKDIR /app

# Start the Django development server
CMD ["python", "manage.py", "runserver", "0.0.0.0:8000"]


