.. _configuration:

#############
Configuration
#############

Network ID: 76

Chain ID: 76

Port: 30313

RPC Port: 8645

WS Port: 8646

RPC TLS Port: 8647

.. code::

    git clone https://github.com/mix-blockchain/mix-blockchain.git

MIX Blockchain can be synchronized with either Geth or Parity:

Geth
----

Install Geth as described here: https://github.com/ethereum/go-ethereum/wiki/Building-Ethereum

.. code::

    geth --config mix.toml --datadir ~/.mix-geth init genesis.json
    geth --config mix.toml --datadir ~/.mix-geth --rpc
    # In a separate terminal launch the console.
    geth attach ~/.mix-geth/geth.ipc

Parity
------

Get Parity from https://parity.io/

.. code::

    parity --chain mix.json --port 30313 --jsonrpc-port 8645 --geth
