FROM python:3.10-slim-buster

# Inside Container
WORKDIR /backend-flask

# Outside container to Inside container
COPY requirements.txt requirements.txt
# Installs the Python libraries within the requirements.txt
RUN pip3 install -r requirements.txt

#From home directory in outside container to inside container
COPY . .

#Creaating and setting the env variables.
ENV FLASK_ENV=development


EXPOSE ${PORT}

#CMD command to run Flask
CMD [ "python3", "-m" , "flask", "run", "--host=0.0.0.0", "--port=4567"]