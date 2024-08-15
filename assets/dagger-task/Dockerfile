FROM docker:dind-rootless

ENV BIN_DIR=$HOME/bin
ENV PATH=$PATH:$BIN_DIR

COPY ./dagger/version .

RUN wget -O - https://dl.dagger.io/dagger/install.sh | DAGGER_VERSION=$(cat version) sh

