FROM golang:1.20 AS builder
RUN mkdir /src
ADD . /src
WORKDIR /src

RUN go env -w GO111MODULE=auto
RUN go build -o main .

FROM gcr.io/distroless/base-debian11

WORKDIR /

COPY --from=builder /src/main /main
EXPOSE 3000
ENTRYPOINT ["/main"]