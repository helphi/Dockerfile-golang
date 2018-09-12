FROM golang:1.11.0-stretch

RUN apt update &&\
    apt install unzip -y &&\
    apt autoremove -y && apt clean && rm -rf /var/lib/apt/lists* /tmp/* /var/tmp/* 

RUN curl -o /usr/local/bin/swagger -L'#' https://github.com/go-swagger/go-swagger/releases/download/0.16.0/swagger_$(echo `uname`|tr '[:upper:]' '[:lower:]')_amd64 &&\
    chmod +x /usr/local/bin/swagger

RUN wget https://github.com/getgauge/gauge/releases/download/v1.0.1/gauge-1.0.1-linux.x86_64.zip &&\
    unzip gauge-1.0.1-linux.x86_64.zip -d /usr/local/bin &&\
    rm -rf gauge-1.0.1-linux.x86_64.zip
    
RUN gauge install screenshot --version 0.0.1 &&\
    gauge install go --version 0.1.2 &&\
    gauge install html-report --version 4.0.5