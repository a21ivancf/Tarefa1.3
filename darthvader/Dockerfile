FROM debian:12

RUN apt update && apt install -y net-tools procps most iproute2 iputils-ping dnsutils

RUN apt install -y bind9 rsyslog

RUN apt clean && rm -rf /var/lib/apt/lists/*

COPY entrypoint.sh /entrypoint.sh

RUN sed -i 's/^OPTIONS=.*/OPTIONS="-u bind -4"/' /etc/default/named

RUN chmod +x /entrypoint.sh
ENTRYPOINT [ "/entrypoint.sh" ]