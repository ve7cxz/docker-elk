FROM alpine:3.8

RUN apk add --no-cache \
      rsyslog=8.34.0-r0 \
      rsyslog-tls \
      && \
    :
COPY . /
VOLUME /var/run/rsyslog/dev
ENTRYPOINT ["rsyslogd", "-n", "-f", "/etc/rsyslogd.conf"]

EXPOSE 514/tcp
EXPOSE 514/udp
