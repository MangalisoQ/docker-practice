# base 
FROM golang:1.16

WORKDIR /usr/src/app

COPY go* ./

RUN go mod download

COPY . .

ENV REDIS_HOST=redis-serv POSTGRES_HOST=db POSTGRES_USER=postgres POSTGRES_PASSWORD=1234 POSTGRES_DATABASE=postgres

RUN go build  .

RUN go test ./...

EXPOSE 5002

CMD ["./server"]

