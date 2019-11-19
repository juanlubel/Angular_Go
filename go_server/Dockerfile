FROM golang:latest

LABEL maintainer="Juanlubel <juanluis.belda@gmail.com>"

RUN mkdir /go/src/go_server
WORKDIR /go/src/go_server

COPY go.mod ./

RUN go mod download

COPY . .

RUN go build -o main .

RUN go get github.com/pilu/fresh
RUN go get -u github.com/kardianos/govendor

EXPOSE 3030

CMD ls -la
