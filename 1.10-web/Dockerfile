FROM golang:1.10.0-stretch

RUN go get github.com/revel/revel &&\
    go get github.com/revel/cmd/revel

RUN apt-key adv --keyserver hkp://pool.sks-keyservers.net --recv-keys 023EDB0B &&\
    echo deb https://dl.bintray.com/gauge/gauge-deb stable main >> /etc/apt/sources.list &&\
    apt-get update &&\
    apt-get install gauge -y &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/* 

RUN gauge install go &&\
    gauge install html-report


