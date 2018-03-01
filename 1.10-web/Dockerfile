FROM golang:1.10.0-stretch

RUN go get github.com/revel/revel &&\
    go get github.com/revel/cmd/revel

RUN apt update &&\
    apt install unzip -y &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/* 

RUN cd /tmp &&\
    wget https://github.com/getgauge/gauge/releases/download/v0.9.7/gauge-0.9.7-linux.x86_64.zip &&\
    unzip gauge-0.9.7-linux.x86_64.zip &&\
    GAUGE_PLUGINS=go,html-report ./install.sh &&\
    rm -rf *


