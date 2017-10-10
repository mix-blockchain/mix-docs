.. _item_store:

Item Store
==========

Item Store is the principle smart contract system for MIX. All base content is registered with Item Store. `IPFS <https://ipfs.io/>`_ is used as the storage layer.

Useful links
------------

* `Source code <https://github.com/link-blockchain/link-item-store>`_

* `Issue tracker <https://github.com/link-blockchain/link-item-store/issues>`_

Properties
----------

Item Store has the following properties:

* Timestamped
   The approximate time that every item is published is recorded on the blockchain.

* World-readable
   Every item published can be read by anyone. The only way to avoid this would be to encrypt the item before publishing it.

* Immutable
    While an item can be "retracted", it can never really be deleted because the transaction that created it will be archived for eternity on full nodes.

* Revisioned
   Item Store has a rudimentary revisioning system built-in where an item can have multiple revisions, e.g. for editing posts. More sophisticated revisioning systems can be built on top of Item Store where each item is a revision.

* Ownership
   Each item can have an owner. Only the owner can modify an item, change item settings, or transfer ownership to another address.

* Configurable
   Each item has the following flags that can be set:

   * Updatable
      The contents of the item can be changed. Once disabled this flag cannot be re-enabled.
   * Enfore Revisions
      When updating the item a new revision must be created. It is not possible to retract revisions. Once enabled, this flag cannot be disabled.
   * Retractable
      The item in its entirety can be retracted. This is unaffected by Enforce Revisions. The itemId of a retracted item can never be used again. Once disabled this flag cannot be re-enabled.
   * Transferable
      The item can be transfered to another user (if they accept it), or disowned completely. Once disabled this flag cannot be re-enabled. At creation time items can also be flagged as anonymous to not have an owner associated. An alternative to transferable items is to use a proxy account with transferable ownership as the item owner.

* Scalable
   Only a bare-minimum of information is stored in contract state. IPFS is used for actual content storage.

* Upgradability
    Item Store is an upgradable system. Due to a security vulnerability, new storage system, or gas cost improvements a new Item Store contract may be deployed.

* Unit tests
   Item Store has tests written in Solidity using the `Dapp <https://dapp.readthedocs.io/>`_ framework.

.. _itemid:


itemId
------

Each item has a 20 byte itemId that is unique to the contract that generated it. The itemId can be further classified to indicate which contract the item is on.

* Off-chain
   There is considered to be an ordered list of Item Store contracts. For example, the first contract would be #0. The next one would be #1. 20 byte itemIds can be prefixed to indicate which contract the item is in, or this can be assumed from context.

   Client software should have a hard coded whitelist of Item Store contracts that its knows how to read from.

* On-chain
   New Item Store contracts register with the Item Store registration contract. When an itemId is stored in a smart contract, it must be stored with the 12 byte Item Store contractId. This way the smart contract can look up the address of any Item Store contract in the registration contract. This is essential to future-proof smart contracts that need to communicate with Item Store contracts.

Deployments
-----------

All current deployments of Item Store contracts on MIX were compiled with Solidity 0.4.16 with optimizations enabled.

Git hash: ``b517451720bcb59d8f731974dfebf80d2ade57d1`` `link <https://github.com/link-blockchain/link-item-store/tree/b517451720bcb59d8f731974dfebf80d2ade57d1>`_


ItemStoreRegistry contract address: ``0x3ea61ec502f053ee89b906fdc3abe2e5f9eb4a7f``

Item Store #0
````````````
IPFS with SHA256 hash.

contract address: ``0x2af783f7d5a607098057ce715b55a82e707a7cab``

BlobStore contractId: ``0xb639900808b2633054720f33``
