FROM quay.io/comp-bio-aging/spark-base:latest

COPY worker.sh /

RUN apt-get update
RUN apt-get install -y rsync

ENV SPARK_WORKER_WEBUI_PORT 8081
ENV SPARK_WORKER_LOG /spark/logs
ENV SPARK_MASTER "spark://spark-master:7077"

EXPOSE 8081

CMD ["/bin/bash", "/worker.sh"]