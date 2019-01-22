.. _configuration:

#############
Configuration
#############

Network ID: 76

Chain ID: 76

MIX Blockchain can be synchronized with either Parity or MIX Geth:

Parity
------

Get Parity from https://www.parity.io/ethereum/
Download the MIX chain specification: https://github.com/mix-blockchain/mix-blockchain/releases/download/v2.1.0/mix.json

.. code::

    parity --chain mix.json --pruning=fast --pruning-history=64 --pruning-memory=0
    
The pruning options are essential to mitigate the risk of a 51% attack.

Geth
----

Download MIX Geth: https://github.com/mix-blockchain/mix-geth/releases

You might need to make the file executable before you can run it, i.e.

.. code::

    chmod +x mix-geth-linux
    ./mix-geth-linux
