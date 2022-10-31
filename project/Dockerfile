# set the base image. Since we're running 
# a Python application a Python base image is used
FROM python:3.8

# maintainer
LABEL maintainer="Oliver Bilstein"

# copy files from the host to the container filesystem. 
COPY ./techtrends /techtrends

#  define the working directory within the container
WORKDIR /techtrends

# install dependencies defined in the requirements.txt file. 
RUN pip install -r requirements.txt

# initialize application database
RUN python init_db.py

# Expose the app port
EXPOSE 3111

# start the application 
CMD [ "python", "app.py" ]
