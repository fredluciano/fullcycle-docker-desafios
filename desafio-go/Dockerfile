FROM golang:1.21 AS builder
WORKDIR /usr/src/app
COPY . .
RUN go build -o build/ main.go

FROM scratch
WORKDIR /usr/src/app
COPY --from=builder /usr/src/app/build .
CMD [ "./main" ]

