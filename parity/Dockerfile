FROM ethereum/client-go:release-1.9
WORKDIR /geth

RUN mkdir data
COPY keys/* /geth/data/keystore/
COPY password /geth/password

ENTRYPOINT ["/usr/local/bin/geth", "--syncmode", "light", "--datadir", "/geth/data", "--rpc", "--rpcaddr", "0.0.0.0", "--rpccorsdomain", "*", "--rpcvhosts", "*", "--nat", "any", "--rpcapi", "eth,web3,personal,net", "--nousb", "--unlock", "0", "--password", "/geth/password", "--allow-insecure-unlock"]
