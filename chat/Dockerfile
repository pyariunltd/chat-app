FROM python:3.8

RUN apt-get update
RUN apt-get install -y python3-dev python3-pip

RUN pip3 install uwsgi 

COPY requirements.txt .

RUN pip3 install -r ./requirements.txt

COPY uwsgi.ini /etc/uwsgi/uwsgi.ini

COPY ./*.py ./

# CMD ["uwsgi", "--ini", "/etc/uwsgi/uwsgi.ini"]

# CMD ["uwsgi", "--http", ":3000", "--gevent", "1000", "--http-websockets", "--master", "--wsgi-file", "wsgi.py", "--callable", "app"]

CMD ["python3", "main.py"]


