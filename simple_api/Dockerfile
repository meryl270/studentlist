FROM python:2.7-stretch
LABEL maintainer="lory.payet@supinfo.com"
#Lancement des maj et installation
RUN apt update
RUN apt install git -y
RUN apt install python-dev python3-dev libsasl2-dev python-dev libldap2-dev libssl-dev -y
RUN pip install flask flask_httpauth flask_simpleldap python-dotenv
#Copie du fichier
COPY student_age.py /
#creation du volume
VOLUME ["/data"]
#copie du fichier dans data
COPY student_age.json /data/
#expose le port 5000
EXPOSE 5000
#lancement du fichier
CMD [ "python", "./student_age.py" ]
