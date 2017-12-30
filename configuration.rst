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

    geth --config mix.toml --datadir ~/.mix-blockchain init genesis.json
    geth --config mix.toml --datadir ~/.mix-blockchain --rpc
    # In a separate terminal launch the console.
    geth attach ~/.mix-blockchain/geth.ipc

Parity
------

Get Parity from https://parity.io/

.. code::

    parity --chain mix.json --port 30313 --jsonrpc-port 8645 --geth

Netstats
--------

To have your node listed on https://stats.mix-blockchain.org/ do the following (requires `Node.js <https://nodejs.org/en/>`_):

.. code::

    git clone https://github.com/cubedro/eth-net-intelligence-api
    cd eth-net-intelligence-api
    npm install
    sudo npm install pm2 -g

Edit app.json::

         {
           "NODE_ENV"        : "production",
           "RPC_HOST"        : "localhost",
    -      "RPC_PORT"        : "8545",
    -      "LISTENING_PORT"  : "30303",
    -      "INSTANCE_NAME"   : "",
    +      "RPC_PORT"        : "8645",
    +      "LISTENING_PORT"  : "30313",
    +      "INSTANCE_NAME"   : "MY_NODE_NAME",      // Customize this.
           "CONTACT_DETAILS" : "",
    -      "WS_SERVER"       : "wss://rpc.ethstats.net",
    -      "WS_SECRET"       : "see http://forum.ethereum.org/discussion/2112/how-to-add-yourself-to-the-stats-dashboard-its-not-automatic",
    +      "WS_SERVER"       : "wss://stats.mix-blockchain.org",
    +      "WS_SECRET"       : "welcometothelinkedworld",
           "VERBOSITY"       : 2
         }

Then::

    pm2 start app.json
