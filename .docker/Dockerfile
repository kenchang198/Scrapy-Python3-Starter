FROM ubuntu:20.04

RUN apt-get update && apt-get install -y --no-install-recommends wget build-essential libreadline-dev \
    libncursesw5-dev libssl-dev libsqlite3-dev libgdbm-dev libbz2-dev liblzma-dev zlib1g-dev uuid-dev libffi-dev libdb-dev \
    libmysqlclient-dev

RUN wget --no-check-certificate https://www.python.org/ftp/python/3.9.5/Python-3.9.5.tgz \
    && tar -xf Python-3.9.5.tgz \
    && cd Python-3.9.5 \
    && ./configure --enable-optimizations\
    && make \
    && make install

RUN apt-get autoremove -y \
    && /usr/local/bin/python3.9 -m pip install --upgrade pip

COPY requirements.txt .
RUN pip3 install -r ./requirements.txt