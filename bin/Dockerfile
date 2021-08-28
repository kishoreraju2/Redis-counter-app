FROM golang:alpine
WORKDIR /app
COPY . .
RUN go build -o demo.bin
EXPOSE 8000
CMD ["./demo.bin"]