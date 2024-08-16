ARG BASE_IMAGE
FROM ${BASE_IMAGE}
USER root

RUN apk update && apk upgrade && apk add -U bash

USER yq

ENTRYPOINT [ "bash" ]
