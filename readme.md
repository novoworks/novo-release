## Supported OS

* debian (>= 10.11)
* ubuntu (>= 20.04)

## Node

### Node configuration

`~/.novo/novo.conf` example:

```
port=8666
rpcport=8665
rpcuser=USERNAME
rpcpassword=PASSWORD
```

### Start node

    $ novod -daemon

### Stop node

    $ novo-cli stop

## Miner

### Miner dependencies

    $ apt install libjansson4 libcurl4

### Miner configuration

`cfg.json` example:

```
{
    "url" : "http://127.0.0.1:8665",
    "user" : "USERNAME",
    "pass" : "PASSWORD",
    "algo" : "sha256dt",
    "threads" : "1",
    "coinbase-addr": "NOVO_ADDRESS"
}
```

**NOVO_ADDRESS**:

    $ novo-cli getnewaddress
    1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa

### Start miner

    $ novominer -c cfg.json

## Novo wallet

    $ novo-cli getbalance
    100.0000

    $ novo-cli sendtoaddress 1A1zP1eP5QGefi2DMPTfTL5SLmv7DivfNa 10.0000

## Docker

    $ docker build -t novo:0.2.0 .
