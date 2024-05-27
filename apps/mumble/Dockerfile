# https://github.com/mumble-voip/mumble
FROM ubuntu:22.04

ARG DEBIAN_FRONTEND=noninteractive

RUN apt-get update && \
    apt-get install -y mumble-server

EXPOSE 64738

CMD ["murmurd", "-fg", "-v"]