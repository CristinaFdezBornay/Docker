# 1. From a debian image:
FROM debian

# 2. Mainteiner:
LABEL maintainer="Cristina Fernandez Bornay"

# 3. Accept the license agreement:
ENV TS3SERVER_LICENSE=accept

# 4. Map the ports to the host (Default voice)
EXPOSE 9987/udp
# 5. Map the ports to the host (Server query)
EXPOSE 10011
# 6. Map the ports to the host (File transport)
EXPOSE 30033

# 7. Update and upgrade:
RUN apt-get -y update && apt-get -y upgrade
# 8. Download the package to download the teamspeak3 server files:
	# RUN apt-get install -y --no-install-recommends apt-utils
RUN apt-get install -y wget
# 9. Download the packege to uncompress [tar command]:
RUN apt-get install -y bzip2

# 10. Download Teamspeak packege
RUN wget http://dl.4players.de/ts/releases/3.7.1/teamspeak3-server_linux_amd64-3.7.1.tar.bz2

# 11. Uncompress and clean the enviroment:
RUN tar -xf teamspeak3-server_linux_amd64-3.7.1.tar.bz2 \
	&& rm teamspeak3-server_linux_amd64-3.7.1.tar.bz2

# 12. Set an entrypoint to launch the server when running the container
ENTRYPOINT sh teamspeak3-server_linux_amd64/ts3server_minimal_runscript.sh

# BUILD:
# docker build -t image_ex01 <path>

# RUN:
# docker run --rm -it -p=9987:9987/udp -p=10011:10011 -p=30033:30033 --name=ex01 image_ex01

# EXEC:
# docker exec -it ex01 /bin/bash

# Teamspeak
# Connec withthe ip of the machine
