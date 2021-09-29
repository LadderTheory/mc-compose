FROM alpine

WORKDIR /app

RUN echo "https://dl-cdn.alpinelinux.org/alpine/edge/testing" >> /etc/apk/repositories

RUN apk add openjdk16
RUN apk add curl
RUN apk add python3

RUN curl https://launcher.mojang.com/v1/objects/a16d67e5807f57fc4e550299cf20226194497dc2/server.jar -o server.jar
RUN touch eula.txt
RUN echo "eula=true" > eula.txt

RUN mkdir server

COPY start.py .

CMD python3 start.py