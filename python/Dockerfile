FROM ubuntu:18.04

# debian:9.5-slim is still on python 3.5.3

RUN useradd node && mkdir -p /home/node && chown -R node:node /home/node

RUN apt-get update && apt-get install -yq python3 --no-install-recommends
CMD [ "python3" ]
