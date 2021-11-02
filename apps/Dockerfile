FROM golang:1.16 as builder
WORKDIR /app
COPY . ./
RUN go build -o ./server-run ./server

FROM gcr.io/distroless/base
EXPOSE 9090

COPY --from=builder app/server-run /.
COPY web /web

CMD [ "./server-run" ]
