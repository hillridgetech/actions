FROM golang:1.15

ENV CI true
RUN curl -sf https://raw.githubusercontent.com/hillridgetech/up/66dbf6d5e8362e1bb008213845a6e01f95917f59/install.sh | sh
RUN chmod +x /usr/local/bin/up

RUN go get github.com/apex/actions/up/cmd/up-wrapper

ENTRYPOINT ["up-wrapper", "deploy", "--no-build"]