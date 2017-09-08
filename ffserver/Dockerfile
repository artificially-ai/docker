FROM debian:latest

RUN apt-get -y update && apt-get install -y vim procps ffmpeg

ADD . /ekholabs/ffserver

WORKDIR ekholabs/ffserver

ENV FFSERVER_FEED_PORT=9090
EXPOSE $FFSERVER_FEED_PORT

ENTRYPOINT ["ffserver"]
CMD ["-d", "-f", "ffserver.conf"]
