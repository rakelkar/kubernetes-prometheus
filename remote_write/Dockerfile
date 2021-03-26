FROM golang:1.15.10

WORKDIR /go/src/app
COPY . .

ENV GO111MODULE=on
RUN bash get.sh
RUN go build

CMD ["./remote_write"]
EXPOSE 1234
