# Teach me about Crucibles

## What is a Crucible?

A Crucible is an ERC-721 NFT \(Non-Fungible Token\) which is minted via[ crucible.alchemist.wtf](https://crucible.alchemist.wtf/) \([How do I mint a Crucible](guides-1/how-do-i-mint-a-crucible.md)\). Crucibles are stored in an Ethereum wallet and can be used as a smart wallet for other ERC20 tokens.

This gives two immediate benefits;

1.  Separate asset management between Crucibles while maintaining a single wallet
2. The ability to transfer your Crucible with it’s contained assets between wallets in a single transaction.

So understanding that a Crucible is able to hold ERC20 tokens, this also opens the possibility to store LP tokens within a Crucible as well. LP tokens are commonly used to participate in staking programs and earn some form of rewards. Taking part in these staking programs would usually mean transferring custody/ownership of your tokens in order to accrue rewards.

Crucibles allow you to do things differently, in addition to being a smart wallet, Crucibles also contain a vault mechanism that allows you to stake your tokens to **non-custodial** reward programs, locking them within the Crucible until you leave a program — i.e. earn rewards without giving up possession of your tokens.

## What is an NFT?

It stands for Non-Fungible Token. "Non-fungible" means "unique" unlike a standard token which shares the same token address, an NFT has it's own unique address.

NFTs are a direct contrast to coins:

* Coins: 1⚗️ is 1⚗️, they have equivalent value and use
* NFTs: a Crucible NFT is not equal to another Crucible NFT and it is very unlikely that any two Crucibles have equivalent value

This is an important point to understand, because people have [already started listing](https://opensea.io/assets/0x54e0395cfb4f39bef66dbcd5bd93cca4e9273d56/620479970925497750675476517677400441094103376596) their Crucibles for sale on platforms such as OpenSea.

It's worth mentioning for the sake of clarity: if you mint a Crucible, you are still also staking ⚗️ in the Uniswap-V2 liquidity pool as well. You are effectively engaging in all 3 ways of potentially earning.

## How do you mint a Crucible?

Originally the only method was getting to grips with the official CLI tool. Fortunately, we've since moved on to having a sophisticated web application which makes the process much easier. The CLI is still available in our GitHub repo however due to the extra risk of making mistakes whilst using the CLI tool it is no longer recommended to take that approach. 

Please use the guide [How do I mint a Crucible?](guides-1/how-do-i-mint-a-crucible.md) to learn the steps to mint your first Crucible.

## What is a Crucible worth?

The value of a Crucible is difficult to determine. The NFT nature of the Crucible could potentially make it have speculative value beyond the its immediate worth, but some Crucibles may be considered more special than others.

Speculation aside, however, what we do know is that a Crucible is created with some variable amount of LP tokens inside, which have an immediately measurable value. 

At a minimum, you could value a crucible based on what you would receive back for unsubscribing its LP contents and trading back to your fiat currency.

Refer to [this section](guides-1/what-can-i-do-with-my-new-crucible.md#checking-how-much-lp-youve-subscribed-to-your-crucible) below for methods to check the contents of a Crucible.

## Should you mint a Crucible?

That is entirely your decision, however there are many benefits for owning and using a Crucible.

#### The cost of minting

When dealing with Ethereum based tokens and contracts you will face gas fees at almost every stage. 

Gas prices continuously fluctuate and this plays a major role on how much gas you are expected to pay, for this reason we are unable to give an indication.

We can say however, that you should take into account the value of your LP tokens against the cost of gas when you are about to submit a transaction to mint a crucible.

#### The tools

Our guides have been based on our wallet of choice, MetaMask. If you need advice regarding the use of other wallets, pop into our [discord](http://discord.alchemist.wtf) channel and the community will be happy to answer.

{% hint style="warning" %}
MetaMask will not recognise or display your Crucible tokens until you [add the token addresses](frequently-asked-questions.md#why-cant-i-see-my-crucible-in-my-wallet) to the application. 
{% endhint %}

## What wallets can I use to store my Crucible?

Crucibles are ERC-721 tokens and signing these transactions are not supported by all Wallet Applications. 

Please refer to our [wallet compatibility guide.](wallet-compatibility.md)

## How many LP tokens do I need to create a Crucible?

Community members have successfully minted a Crucible with as low as 0.01 LP tokens.

Of course, a Crucible still costs gas to mint, so please take into consideration this cost when creating one with minimal LP.

Remember, you earn rewards proportional to your LP share of the total LP staked in the Aludel.

## Can I create multiple Crucibles?

Yes you can. Many users in the community have already minted multiple Crucibles, at the time of writing there are more than 12% of users with multiple Crucibles.

## How can I check how many LP tokens someone else's Crucible is worth?

You can take the Crucible's token ID, convert it into hexadecimal \(if it is in decimal\) and then search for the address on [etherscan.io](https://etherscan.io).

This will display what the contents are and the history of transactions that have occurred within the Crucible.

If you can't see any tokens displayed for it, then it's most likely empty.

## How do I view my tokens on MetaMask?

Refer to [our FAQ ](https://app.gitbook.com/@alchemist-docs/s/crucible/frequently-asked-questions)on the addresses that you need to add to your wallet to be able to see the token.

