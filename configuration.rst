.. _configuration:

#############
Configuration
#############

Network ID: 76

Chain ID: 76

MIX Blockchain can be synchronized with either Geth or Parity:

Parity
------

Get Parity from https://www.parity.io/ethereum/
Download the MIX chain specification: https://github.com/mix-blockchain/mix-blockchain/releases/download/v2.0.0/mix.json

.. code::

    parity --chain mix.json

Geth
----

Download MIX Multi-geth: https://github.com/mix-blockchain/multi-geth/releases

You might need to make the file executable, i.e.

.. code::

    chmod +x mix-geth-linux

Use the parameter --mix, i.e.

.. code::

    ./mix-geth-linux --mix
