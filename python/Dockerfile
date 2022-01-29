FROM python:3.8-buster

ENV MQ_JUPYTER_TOKEN=abc
ENV MQ_BASE_URL=http://host.docker.internal:9042/api/
ENV MQ_STACK_HASH=xyz

ENV MQ_USER_NAME="Donald Duck"
ENV MQ_USER_EMAIL="donald@duckburg.com"

EXPOSE 8888

RUN mkdir /opt/notebook \
    && pip install jupyter \
    && git config --global user.name ${MQ_USER_NAME} \
    && git config --global user.email ${MQ_USER_EMAIL}

ADD samples /opt/notebook/samples

CMD /bin/bash -c "cd /opt/notebook && jupyter notebook --no-browser --allow-root --NotebookApp.allow_origin='*' --NotebookApp.ip='0.0.0.0' --NotebookApp.token='${MQ_JUPYTER_TOKEN}'"
