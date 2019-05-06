FROM ubuntu:16.04

LABEL description="Devspaces implementation for SLI Libraries Assembler"

ENV LANG=C.UTF-8

RUN apt-get update && \
    apt-get install -y apt-utils \
    build-essential \
    chrpath \
    curl \
	dialog \
    git \
    libssl-dev \
    libxft-dev \
    libfreetype6 \
    libfreetype6-dev \
    libfontconfig1 \
    libfontconfig1-dev \
    mc \
    net-tools \
	sudo \   
    vim\
    wget && \
    curl -sL https://deb.nodesource.com/setup_8.x | sudo -E bash - && \
 	apt-get update && \
	apt-get install -y nodejs && \
    apt-get clean && \
    wget https://bitbucket.org/ariya/phantomjs/downloads/phantomjs-2.1.1-linux-x86_64.tar.bz2 && \
    tar xvjf phantomjs-2.1.1-linux-x86_64.tar.bz2 -C /usr/local/share/ && \
    ln -s /usr/local/share/phantomjs-2.1.1-linux-x86_64/bin/phantomjs /usr/local/bin/         

WORKDIR /data

EXPOSE 9000 3001

CMD tail -f /dev/null
