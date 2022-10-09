FROM debian:11.1-slim
LABEL maintainer="Vincent(46603415@qq.com)"
RUN mkdir -p /app/
ADD time-sync /app/time-sync
ADD conf.yaml /app/conf.yaml
EXPOSE 7100
WORKDIR "/app"
CMD ["/app/time-sync"]

