FROM python:3.7-alpine

ENV PORT 5000

COPY files/requirements.txt /
COPY files/run.sh /

RUN apk --no-cache --update add g++ make && \
    pip --no-cache-dir install --upgrade -r /requirements.txt && \
    rm -rf /requirements.txt

ENTRYPOINT ["/run.sh"]
