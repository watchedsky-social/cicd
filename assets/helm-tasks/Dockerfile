FROM cgr.dev/chainguard/go:latest-dev AS collect

RUN ["go", "install", "github.com/davidrjonas/semver-cli@latest"]
RUN ["go", "install", "github.com/mikefarah/yq/v4@latest"]
RUN ["go", "install", "helm.sh/helm/v3/cmd/helm@latest"]

FROM cgr.dev/chainguard/glibc-dynamic:latest-dev AS release

USER root
COPY --from=collect /root/go/bin/* /usr/bin
ENTRYPOINT [ "bash" ]
