Mixin Registry
==============

`Source <https://github.com/mix-blockchain/mix-mixin-registry/blob/master/src/mix_mixin_registry.sol>`_

Deployment address: ``0x99be57fca49270b69306cdbe89df416d769dbd06``

Solidity 0.4.16 with optimizations.

 
Every item of content stored on MIX is composed of one or more mixins. Examples of potential content types are tweets, comments, blog posts, media metadata and user profiles.

MIX has a hierarchical system of mixins. There is a `root mixin <https://github.com/mix-blockchain/mix-root-mixin-schema/tree/c578af35b77246027beebb004a65b951475f577e>`_ that all other mixins are derived from.

Each mixin is identified by an integer, the mixinId. The mixinId for each mixin is issued by the Mixin Registry smart contract. The mixinId of the root mixin is 0.

When creating a new mixin, the `addMixin() <https://github.com/mix-blockchain/mix-mixin-registry/blob/master/src/mix_mixin_registry.sol#L60>`_ method must be called. ``parent`` must be the mixinId of the mixin that is being extending. ``uri`` should be a link to an immuntable commit in a repo that is derived from the parent mixin.
