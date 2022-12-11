FROM ubuntu
USER root
ENV PYTHONUNBUFFERED=1
RUN sudo apt-get update -y
RUN sudo apt-get upgrade -y
RUN sudo apt-get install python3.10 -y
WORKDIR /gallishop
COPY . .
RUN pip3 install -r requirements.txt
#CMD [ "python3", "manage.py", "runserver", "0.0.0.0:8000" ]