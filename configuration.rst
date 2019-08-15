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

.. code::

    chmod +x parity
    ./parity --chain mix --pruning=fast --pruning-history=64 --pruning-memory=0
    
The pruning options are essential to mitigate the risk of a 51% attack.

Geth
----

Download MIX Geth: https://github.com/mix-blockchain/mix-geth/releases

.. code::

    chmod +x mix-geth-linux
    ./mix-geth-linux
