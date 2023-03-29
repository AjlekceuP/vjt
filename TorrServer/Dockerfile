FROM ubuntu:22.10

RUN apt update \
    && apt upgrade -y \
    && apt install -y wget

RUN mkdir -p /torrserver/db/ \
    && wget -O /torrserver/TorrServer "https://github.com/YouROK/TorrServer/releases/download/MatriX.120/TorrServer-linux-amd64" \
    && chmod +x /torrserver/TorrServer

EXPOSE 8090:8090

VOLUME /torrserver/db/

ENTRYPOINT ["/torrserver/TorrServer", "-d" , "/torrserver/db/"]