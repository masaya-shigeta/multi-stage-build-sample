FROM golang:1.18
WORKDIR /go/src/app
COPY main.go go.mod go.sum ./
RUN CGO_ENABLED=0 GOOS=linux go build -o main .

FROM alpine:latest
WORKDIR /root/
COPY --from=0 /go/src/app/main ./
CMD ["./main"]
