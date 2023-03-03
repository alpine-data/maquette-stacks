FROM python:3.10.2-bullseye

ADD run_mlflow.sh /opt/run_mlflow.sh

RUN \
    pip install mlflow=="1.30.0" boto3 psycopg2-binary && \
    chmod +x /opt/run_mlflow.sh

CMD /opt/run_mlflow.sh