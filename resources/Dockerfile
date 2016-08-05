FROM alpine

ENV TERM xterm
ENV http_proxy http://proxy.nuvemluiza.intranet:8080
ENV https_proxy http://proxy.nuvemluiza.intranet:8080

EXPOSE 8080

RUN apk update
RUN apk add bash
RUN apk add nano
RUN apk add openjdk8

ADD romaneio /apps/apis/romaneio
RUN chmod u=rwx,g=rx,o-rwx /apps/apis/romaneio/run.sh

CMD /apps/apis/romaneio/run.sh