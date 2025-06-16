# FROM golang:1.17

# WORKDIR /go/src/app

# COPY *.go .

# RUN go mod init dispatch && go get
# RUN go install

# CMD dispatch

FROM golang:latest

WORKDIR /go/src/app

COPY *.go .

RUN go mod init dispatch && go mod tidy
RUN go build -o dispatch .

CMD ["./dispatch"]
