FROM ubuntu:18.04

RUN apt-get update && apt-get -y update
RUN apt-get install -y build-essential python3.6 python3-pip python3-dev
RUN pip3 -q install pip --upgrade
RUN pip3 install jupyter

RUN mkdir src
WORKDIR src/
COPY . .

RUN pip3 install -r requirements.txt

CMD ["jupyter", "notebook", "--port=2222", "--no-browser", "--ip=0.0.0.0", "--allow-root"]
