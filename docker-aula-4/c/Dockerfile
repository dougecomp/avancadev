FROM golang:1.15

WORKDIR /go/src/avancadev

COPY . .

RUN go get -d -v ./
RUN go install -v ./

RUN GOOS=linux go build -ldflags="-s -w"

EXPOSE 9090

ENTRYPOINT ["./avancadev"]