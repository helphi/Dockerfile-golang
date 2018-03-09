FROM golang:1.10.0-stretch

RUN apt update &&\
    apt install unzip -y &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/* 

RUN curl -SsL https://downloads.gauge.org/stable | sh &&\
    gauge install screenshot &&\
    gauge install go &&\
    gauge install html-report

RUN go get github.com/go-swagger/go-swagger/cmd/swagger


