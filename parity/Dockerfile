FROM parity/parity:v2.7.2-stable
USER root

RUN mkdir -p /parity

WORKDIR /parity

RUN apt-get update -y
RUN apt-get install -y curl bash software-properties-common

COPY ./entrypoint-parity.sh .

ARG PARITY_ID
RUN echo "Building parity${PARITY_ID}..."

COPY ./password       password
COPY ./parity.toml    parity.toml
COPY ./key/*          ./keys/ethereum/

ENTRYPOINT [ "bash", "./entrypoint-parity.sh" ]
