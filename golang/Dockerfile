FROM golang:stretch
RUN apt-get update
RUN apt-get install -y apt-utils \
    && apt-get install -y vim \
    && apt-get install -y telnet \
    && apt-get install -y iputils-ping \
    && apt-get install -y curl \
    && apt-get install -y procps \
    && apt-get install -y supervisor

COPY config/supervisord.conf /etc/supervisor/conf.d/supervisord.conf
RUN mkdir -p /opt/code
CMD /usr/bin/supervisord

# RUN mkdir /files
# COPY hw.go /files
# WORKDIR /files
# RUN go build -o /files/hw hw.go ENTRYPOINT ["/files/hw"]
