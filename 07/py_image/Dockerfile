FROM ubuntu:14.04
ADD requirements.txt /tmp/
RUN apt-get update
RUN DEBIAN_FRONTEND=noninteractive apt-get install -y -q python-all python-pip
RUN pip install -qr /tmp/requirements.txt
ADD app.py /opt/webapp/
EXPOSE 5000
CMD ["python", "/opt/webapp/app.py"]