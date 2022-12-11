FROM ubuntu:jammy
USER root
ENV PYTHONUNBUFFERED=1
RUN apt-get update -y
RUN apt-get install dialog apt-utils -y
RUN echo 'debconf debconf/frontend select Noninteractive' | debconf-set-selections
RUN apt-get upgrade -y
RUN apt-get install -y -q
RUN apt-get install python3.9 -y
RUN apt-get install python3-pip -y
WORKDIR /gallishop
COPY . .
RUN pip3 install -r requirements.txt
#CMD [ "python3", "manage.py", "runserver", "0.0.0.0:8000" ]