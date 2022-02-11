FROM ubuntu:18.04

RUN apt-get update && apt-get -y update
RUN apt-get install -y build-essential python3.6 python3-pip python3-dev
RUN pip3 -q install pip --upgrade
RUN pip3 install jupyter

RUN mkdir src
WORKDIR src/
COPY . .

RUN pip3 install -r requirements.txt

CMD ["jupyter", "notebook", "--port=1234", "--no-browser", "--ip=0.0.0.0", "--allow-root"]


# syntax=docker/dockerfile:1
# FROM python:3.7-alpine
# WORKDIR /code
# ENV FLASK_APP=app.py
# ENV FLASK_RUN_HOST=0.0.0.0
# RUN apk add --no-cache gcc musl-dev linux-headers
# COPY requirements.txt requirements.txt
# RUN pip install -r requirements.txt
# EXPOSE 5000
# COPY . .
# CMD ["flask", "run"]
