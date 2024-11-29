FROM ubuntu:20.04

WORKDIR /app

RUN apt-get update
RUN apt-get install -y software-properties-common

COPY . .

RUN chmod +x brokerFileManager

EXPOSE 32002

CMD ./brokerFileManager -D FOREGROUND