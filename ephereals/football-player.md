---
description: 'Official contract address: 0xF48b4c5E2C7115Fb696b5401648D47E07a83194C'
---

# Model

In Ephere, football players are non-fungible, transferable, and scarce digital assets stored in a smart contract implementing the ERC-721 standard (also known as NFT) in the [Binance Smart Chain](https://coinmarketcap.com/alexandria/article/what-is-binance-smart-chain).

They have mental and physical attributes, trainable football skills that are capped by genetic and distinctive visual properties, some of which can be changed by their owner. Players gain experience by playing matches, and they can also get tired, injured, grow old, and retire — _they’re alive_.

{% hint style="info" %}
Official contract: [0xF48b4c5E2C7115Fb696b5401648D47E07a83194C](https://bscscan.com/token/0xF48b4c5E2C7115Fb696b5401648D47E07a83194C) ([Source code](https://github.com/ephere-football/contracts/blob/master/contracts/EphereFootballerERC721.sol))
{% endhint %}

### Attributes & skills

We want Ephere to be a fun game in which people can express their creativity, ingenuity, and strategic thinking to maximize their chance of success. To accomplish that we need a sophisticated football match simulation engine with the capacity to simulate a wide range of football situations, which requires a complex football player data model. That’s why our players have a broad set of attributes that describe several aspects of their uniqueness:

{% embed url="https://gist.github.com/agurodriguez/7bfb9a0683f0b5e08baf36451e146c96#file-ephere-football-player-csv" %}

**Layer-1 attributes** are defined when the player is created and can't change afterward. The data is written in the blockchain and no one (not even us) can modify it. The vast majority of the mental, physical, and technical _limits_ of the player such as Determination, Stamina, or Finishing skill, are L1 attributes.

**Layer-2 attributes** can suffer fluctuations based on in-game activity. The data is written in Ephere's servers. Age, Energy, Experience are some examples of layer-2 attributes. Mental, physical, and technical attributes are also layer-2 attributes, meaning they represent the skill limit at layer-1, and the current value at layer-2. This means that you can perform in-game actions to increase (or decrease) their value. These are some examples:

* When you perform a training session to improve the Marking skill of a football player, the value of the layer-2 attribute will sightly increase, but the value of the layer-1 attribute will be left untouched. In other words, the value of the actual Marking will sightly increase, but the maximum value of the Marking skill will be the same. Of course, the value of the attribute at layer-2 cannot be greater than the value at layer-1.

{% hint style="warning" %}
In the future we'll use a High-Throughput blockchain --probably built by us-- to store layer-2 attributes.
{% endhint %}

### Retirement

As players get old their performance decrease. Users will be able to retire their players if they want, leaving room for new players to be born (Remember, players are scarce). For doing so they will be rewarded.

{% hint style="warning" %}
Retiring a player implies burning the ERC721 token.
{% endhint %}
