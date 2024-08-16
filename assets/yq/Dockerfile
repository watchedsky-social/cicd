ARG BASE_IMAGE
FROM ${BASE_IMAGE}
USER root

RUN apk update && apk upgrade && apk add -U bash

ENTRYPOINT [ "bash" ]
