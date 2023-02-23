FROM python:3.10-slim-buster

# Inside Container
# make a new folder inside the container
WORKDIR /backend-flask

# Outside Container - - > Inside Container
# This contains the libraries we want to install
COPY requirements.txt requirements.txt

# Inside Container
# Install the python libraries used for the app
RUN pip3 install -r requirements.txt

#  Outside Container - - > Inside Container
# '.' means everything in the current directory
# First period '.' represents /backend-flask (Outside the container)
# 2nd period '.' represents /backend-flask (Inside the container)
COPY . .

ENV FLASK_ENV=development

EXPOSE ${PORT}
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]