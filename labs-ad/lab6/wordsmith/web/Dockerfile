FROM golang:1.21-alpine AS build

WORKDIR /app

COPY . .

RUN go build -o dispatcher dispatcher.go

FROM alpine:3.18

WORKDIR /app

COPY --from=build /app/dispatcher .

COPY static ./static

EXPOSE 8080

CMD ["./dispatcher"]