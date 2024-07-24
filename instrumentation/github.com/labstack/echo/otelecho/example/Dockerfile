# Copyright The OpenTelemetry Authors
# SPDX-License-Identifier: Apache-2.0
FROM golang:1.23rc2-alpine3.20 AS base
COPY . /src/
WORKDIR /src/instrumentation/github.com/labstack/echo/otelecho/example

FROM base AS echo-server
RUN go install ./server.go
CMD ["/go/bin/server"]
