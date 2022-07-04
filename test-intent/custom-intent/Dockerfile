FROM golang:1.18-alpine3.15
WORKDIR /app

RUN apk add --update make
COPY go.* ./
RUN go mod download

COPY . ./
RUN go build -o /server
CMD '/server'