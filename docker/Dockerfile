FROM tensorflow/tensorflow:1.15.5-gpu-py3
RUN pip install bert-serving-server[http]
COPY ./docker/entrypoint.sh /app
WORKDIR /app
ENTRYPOINT ["/app/entrypoint.sh"]
CMD []
HEALTHCHECK --timeout=5s CMD curl -f http://localhost:8125/status/server || exit 1
