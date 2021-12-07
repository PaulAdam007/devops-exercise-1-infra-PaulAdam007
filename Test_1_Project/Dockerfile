FROM ubuntu
LABEL  Author='paul adams'
# Creating Application Source Code Directory

RUN mkdir -p /usr/src/app
RUN apt-get update
RUN apt-get install -y python
# Setting Home Directory for containers
WORKDIR /usr/src/app

# Installing python dependencies
##COPY requirements.txt /usr/src/app/
#RUN pip install --no-cache-dir -r requirements.txt

# Copying src code to Container
COPY . /usr/src/app

# Application Environment variables
#ENV APP_ENV development
ENV PORT 9091

# Exposing Ports
EXPOSE $PORT

# Setting Persistent data
#VOLUME ["/app-data"]

# Running Python Application
CMD ["/usr/src/app/app.py"]
ENTRYPOINT ["python"]
