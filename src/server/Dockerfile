FROM ubuntu:20.04

WORKDIR /app

RUN apt-get update
RUN apt-get install -y software-properties-common curl

COPY . .

RUN chmod +x serverFileManager

EXPOSE 32001

RUN mkdir FileManagerDir

# ip del broker | puerto del broker | ip del server | puerto del server
CMD SERVER_IP=$(curl -s https://api.ipify.org) && ./serverFileManager ${BROKER_IP} 32002 ${SERVER_IP} 32001