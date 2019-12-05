FROM ubuntu as google
RUN apt-get update -y 
RUN apt-get install curl -y
RUN curl https://www.google.com > google.txt

FROM alpine:latest
COPY --from=0 google.txt /
CMD wc -c google.txt

