FROM minio/minio:RELEASE.2022-01-08T03-11-54Z

EXPOSE 9000
RUN mkdir -p /data/mlflow
ENTRYPOINT []
CMD ["/usr/bin/minio", "server", "/data"]