FROM golang:1.21 AS build
WORKDIR /app
COPY . .
RUN go build -o dispatcher dispatcher.go


FROM golang:1.21-alpine
WORKDIR /app
COPY --from=build /app/dispatcher .
COPY static ./static
CMD ["./dispatcher"]
