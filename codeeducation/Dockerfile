FROM golang:1.18.0-alpine AS builder

WORKDIR /usr/src/app

COPY . ./
RUN go mod download

RUN go build -o /codeeducation

FROM scratch
COPY --from=builder /codeeducation /codeeducation

CMD [ "/codeeducation" ]
