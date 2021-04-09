FROM python:buster

RUN groupadd -r mcrsrvc -g 433 && \
    mkdir /usr/local/mcrsrvc && \
    useradd -u 431 -r -g mcrsrvc -d /usr/local/mcrsrvc -s /sbin/nologin -c "Micro Service User" mcrsrvc

ADD requirements.txt /usr/local/mcrsrvc/requirements.txt
ADD helloworld.py /usr/local/mcrsrvc/helloworld.py

WORKDIR /usr/local/mcrsrvc


RUN pip3 install -r ./requirements.txt

USER 431

CMD ["python3","helloworld.py"]
