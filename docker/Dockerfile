FROM canerdogan/talib

ADD . /app
WORKDIR "/app"

RUN apt-get install -y python3-dev

RUN ln -s /usr/bin/pip3 /usr/bin/pip
RUN ln -s /usr/bin/python3 /usr/bin/python
RUN pip install --upgrade pip
RUN pip install setuptools

RUN pip install -r /app/requirements.txt
RUN pip install /app

VOLUME ["/app"]

RUN /bin/bash