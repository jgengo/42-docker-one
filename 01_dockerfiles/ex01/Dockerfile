FROM debian
MAINTAINER jgengo <jgengo@student.42.fr>

EXPOSE 9987/udp 30033 10011

RUN apt-get update \
	&& apt-get install wget bzip2 wget ca-certificates -y \
	&& adduser --disabled-password --gecos "" teamspeak

WORKDIR /home/teamspeak

RUN wget http://dl.4players.de/ts/releases/3.0.11.1/teamspeak3-server_linux-amd64-3.0.11.1.tar.gz \
	&& tar -xzvf *.tar.gz && rm *.tar.gz

WORKDIR teamspeak3-server_linux-amd64

CMD ["sh", "ts3server_minimal_runscript.sh"]