FROM golang:1.18-alpine
WORKDIR /go/src/app

COPY main.go go.mod go.sum ./
RUN CGO_ENABLED=0 GOOS=linux go build -o /go/src/app/main
CMD ["/go/src/app/main"]
