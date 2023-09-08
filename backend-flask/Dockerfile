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

#Running the container 
#FRONTEND_URL="*" BACKEND_URL="*" docker run --rm -p 4567:4567 -it backend-flask

#docker run --rm -p 4567:4567 -it -e FRONTEND_URL='*' -e BACKEND_URL='*' backend-flask