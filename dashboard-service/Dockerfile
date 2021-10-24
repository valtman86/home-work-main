FROM alpine:3.7
WORKDIR /app
ADD . /app
EXPOSE 9002
ENV PORT 9002
ENV COUNTING_SERVICE_URL http://counting-service:9001
CMD ["./dashboard-service"]
