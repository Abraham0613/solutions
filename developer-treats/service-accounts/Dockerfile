# Dockerfile to build an image with op installed and token set for Service Accounts
FROM alpine
ENV OP_CLI_VERSION v2.18.0
ENV ARCH amd64
ENV OP_SERVICE_ACCOUNT_TOKEN="yourtoken"

RUN apk add curl unzip

RUN curl -sSfo op.zip https://cache.agilebits.com/dist/1P/op2/pkg/${OP_CLI_VERSION}/op_linux_${ARCH}_${OP_CLI_VERSION}.zip \
  && unzip -od /usr/local/bin/ op.zip \
  && rm op.zip
