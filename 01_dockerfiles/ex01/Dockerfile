FROM debian
MAINTAINER sechang <sechang@student.42.us.org>

ENV TS3SERVER_LICENSE=accept

RUN apt-get update && apt-get upgrade
RUN apt-get install -y wget bzip2

RUN wget https://files.teamspeak-services.com/releases/server/3.6.1/teamspeak3-server_linux_amd64-3.6.1.tar.bz2
RUN tar xfvj teamspeak3-server_linux_amd64-3.6.1.tar.bz2
EXPOSE 9987/udp 10011 30033
  # Port 9987/udp is default TeamSpeak 3 server port
  # Port 10011 is used for Server Query
  # Port 30033 is used for File transfer

WORKDIR teamspeak3-server_linux_amd64

ENTRYPOINT sh ts3server_minimal_runscript.sh



#Setup a TeamSpeak 3 Server on Linux (Ubuntu / Debian):
#article is good. teamspeak version is too old.
#https://www.unixblogger.com/setup-a-teamspeak-3-server-on-linux-ubuntu-debian/
#How to build it?
#docker build -t ex01 .
#How to run it?
#docker run -it --rm --name teamspeak3 -e TS3SERVER_LICENSE=accept -p 9987:9987/udp -p 10011:10011 -p 30033:30033 ex01
#use TeamSpeak 3, connect to server, ip is the Char ip
