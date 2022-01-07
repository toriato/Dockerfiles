FROM mcr.microsoft.com/java/jre:17-zulu-alpine
ENV UID=1000
ENV GID=$UID

COPY ./startup /startup
RUN chmod +x /startup
RUN apk add --no-cache bash curl jq

USER $UID
WORKDIR /data

ENTRYPOINT ["/startup"]

