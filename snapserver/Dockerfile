FROM alpine:3.12

RUN apk update
RUN apk add ca-certificates
RUN apk add wget
RUN apk add snapcast-server

RUN /usr/bin/snapserver -v
COPY snapserver.conf /etc/snapserver.conf
COPY index.html /www/index.html
EXPOSE 1704 1705 1780
ENTRYPOINT ["/bin/bash","-c","/usr/bin/snapserver"]
