FROM python:3.10-slim-buster

#Inside Container
#Make a new folder inside container
WORKDIR /backend-flask

#Outside Container -->Inside Container
#This contains the libraries want to install to run app
COPY requirements.txt requirements.txt

#Inside Container
#Install the python images use for the apps
RUN pip3 install -r requirements.txt

#Outside Container -->Inside Container 
# . means everything in the current directory
# first period . -/backen-flask outside container
# secon period . /backend-flask inside container 
COPY . .


#Set Environment Variables ( Env Vars)
#Inside container will remain set when the container is run
ENV FLASK_ENV=development

EXPOSE ${PORT}

#CMD COMMAND
#python3 -m flask run --host=0.0.0.0 --port=4567
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]