FROM alpine:latest

RUN apk update
RUN apk add --no-cache git perl
RUN cd /tmp
RUN git clone https://github.com/jasonm23/cowsay.git
RUN cd cowsay ; ./install.sh /usr/local
RUN cd /
RUN rm -rf /tmp/*
RUN apk del git

CMD [ "/usr/local/bin/cowsay","Hello word!" ]