FROM golang

COPY docker-entrypoint.sh /

RUN go get -v github.com/cloudfoundry/java-buildpack-memory-calculator &&\
    cd src/github.com/cloudfoundry/java-buildpack-memory-calculator &&\
    go get -v github.com/tools/godep && \
    chmod +x /docker-entrypoint.sh

ENTRYPOINT ["/docker-entrypoint.sh"]