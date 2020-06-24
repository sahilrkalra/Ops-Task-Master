FROM golang:1.12

RUN mkdir app
WORKDIR app

COPY . .

ENV DEMO_APP_ADDR :8000
ENV DEMO_REDIS_ADDR redis:6379

RUN make build

CMD ["make", "run"]