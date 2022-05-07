# Reward Program Mechanics

The reward programs utilise a share based reward mechanism that has 2 main scaling mechanisms that are used to protect the reward program and to create longer term alignment/incentivisation with the participants.

There are no forced staking periods or reward vesting in our contracts, the programs were designed so users are free to enter and leave as they wish.

### **Multiplier**

This is a scaling mechanism that grows scales a users entitlement of rewards up to their full % of the pool that they are entitled to.

The multiplier contains 2 aspects - the min/max multiplier and the scaling duration.

#### Example

> Reward program is configured to be: `1x` to `10x` over `10 days`
>
> A user has staked 10% of the staking tokens in the program; the multiplier mechanism means that they would not be eligible for 10% of the tokens in the reward pool straight away, they would need to scale up to that over the defined period.
>
> If the users share of the pool should be around 10 MIST, the multiplier in this example will make the user only be able to access 1 MIST at day 1, 2 MIST at day 2 etc.

_**As the program is share based, a users share of the pool can also change depending on the activity of other users.**_

### **Funding**

This has a reward funding release mechanism that can be used to release the reward tokens to users over a set amount of time. Funding an Aludel requires a smart contract call for the 'Reward Token', bonus tokens can be dropped directly into the Aludel pool without any contract call required, the bonus token share will be calculated based on the users share of the main Reward token.

Using the Aludel v1.5 for example, we deposit into our Aludel every 14 days and have defined a release period of 1209600 seconds (14 days).

#### Example

> You fund a program 864000 tokens over 10 days (864000 seconds)\
> \
> The program will release 1 token per second that can be redeemed. \
> \
> The distribution of that token will depend on a users current eligibility of % of pool based on their multiplier and share size

Using the Multiplier and Funding release mechanisms in conjunction with each other is beneficial to create longer term alignment and will provide a scaling experience to the user.

### **Token Support**

The reward program contracts only support ERC20 tokens, so, for example, Uniswap V3 positions (NFTs) wouldn't be supported. Any ERC20 token to be subscribed/staked (except rebasing tokens). Rebasing tokens can be used as reward tokens and the program can support up to 50 different tokens.

These two articles might be useful to see the process and understand about Crucibles/Aludels a bit further:

[https://docs.alchemist.wtf/crucible/guides-1/how-do-i-mint-a-crucible ](https://docs.alchemist.wtf/crucible/guides-1/how-do-i-mint-a-crucible)[https://medium.com/alchemistcoin/crucible-and-aludel-explainer-86c3e6e5c49c](https://medium.com/alchemistcoin/crucible-and-aludel-explainer-86c3e6e5c49c)
