ARG BASE_IMAGE=cgr.dev/chainguard/go:latest-dev
FROM ${BASE_IMAGE} AS collect

RUN ["go", "install", "github.com/davidrjonas/semver-cli@latest"]
RUN ["go", "install", "github.com/mikefarah/yq/v4@latest"]
RUN ["go", "install", "helm.sh/helm/v3/cmd/helm@latest"]

FROM cgr.dev/chainguard/git:latest-root-dev AS release

COPY --from=collect /root/go/bin/* /usr/bin
RUN apk update && apk add -U curl
ENTRYPOINT [ "bash" ]
