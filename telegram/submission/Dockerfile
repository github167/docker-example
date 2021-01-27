FROM python:rc-alpine

WORKDIR /opt

COPY ./main.py /opt
COPY config.json /opt
COPY data.json /opt

RUN apk add --no-cache --virtual .build-deps libressl-dev build-base libffi-dev && pip install python-telegram-bot --upgrade && apk del .build-deps

CMD ["python3", "main.py"]
