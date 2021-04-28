FROM --platform=$BUILDPLATFORM golang:1.16

ARG BUILDPLATFORM

RUN go get github.com/codegangsta/gin

RUN mkdir /app

ADD . /app

WORKDIR /app

RUN rm -rf /app/vendor
RUN go mod vendor

RUN go build -o main .

ENV TZ=Asia/Jakarta

CMD ["/app/main"]