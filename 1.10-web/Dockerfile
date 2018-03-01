FROM golang:1.10.0-stretch

RUN go get github.com/revel/revel &&\
    go get github.com/revel/cmd/revel

RUN apt update &&\
    apt install unzip -y &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/* 

RUN curl -SsL https://downloads.gauge.org/stable | sh &&\
    gauge install go &&\
    gauge install html-report


