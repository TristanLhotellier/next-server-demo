# find the latest minecraft-server.jar file from https://www.minecraft.net/en-us/download/server
FROM ubuntu

RUN apt-get update && \
    apt-get install -y openjdk-21-jre-headless wget ca-certificates && \
    rm -rf /var/lib/apt/lists/*

WORKDIR /app

RUN wget https://piston-data.mojang.com/v1/objects/145ff0858209bcfc164859ba735d4199aafa1eea/server.jar -O server.jar

RUN echo "eula=true" > eula.txt

EXPOSE 25565

CMD ["java", "-Xmx1024M", "-Xms1024M", "-jar", "server.jar", "nogui"]