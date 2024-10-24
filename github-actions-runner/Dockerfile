FROM ubuntu:22.04

ARG runner_version="2.320.0"

ARG DEBIAN_FRONTEND=noninteractive

RUN apt update -y && apt upgrade -y && useradd -m docker
RUN apt install -y --no-install-recommends \
    curl jq build-essential libssl-dev libffi-dev python3 python3-pip python3-venv python3-dev

RUN cd /home/docker && mkdir actions-runner && actions-runner \
    && curl -O -L https://github.com/actions/runner/releases/download/v${runner_version}/actions-runner-linux-x64-${runner_version}.tar.gz \
    && tar xzf ./actions-runner-linux-x64-${runner_version}.tar.gz 

RUN chown -R docker ~docker && /home/docker/actions-runner/bin/installdependencies.shared

COPY start.sh start.sh

RUN chmod +x start.sh

USER docker

ENTRYPOINT [ "./start.sh" ]

