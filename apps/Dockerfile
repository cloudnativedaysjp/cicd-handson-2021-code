FROM golang:latest
WORKDIR /app
COPY . ./
RUN go build -o ./server-run ./server
EXPOSE 9090
CMD [ "./server-run" ]
