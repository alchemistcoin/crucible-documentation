# Reward Program Contracts

## **Mechanics**

The reward programs utilise a share based reward mechanism that has 2 main scaling mechanisms that are used to protect the reward program and to create longer term alignment/incentivisation with the participants.

There are no forced staking periods or reward vesting in our contracts, the programs were designed so users are free to enter and leave as they wish.

### **Multiplier**

This is a scaling mechanism that grows scales a users entitlement of rewards up to their full % of the pool that they are entitled to.

The multiplier contains 2 aspects - the min/max multiplier and the scaling duration.

Example ``Reward program is configured to be: `1x` to `10x` over `10 days` A user has staked 10% of the staking tokens in the program; the multiplier mechanism means that they would not be eligible for 10% of the tokens in the reward pool straight away, they would need to scale up to that over the defined period. If the users share of the pool should be around 10 MIST, the multiplier in this example will make the user only be able to access 1 MIST at day 1, 2 MIST at day 2 etc.``

_**As the program is share based, a users share of the pool can also change depending on the activity of other users.**_

### **Funding**

This has a reward funding release mechanism that can be used to release the reward tokens to users over a set amount of time. Funding an Aludel requires a smart contract call for the 'Reward Token', bonus tokens can be dropped directly into the Aludel pool without any contract call required, the bonus token share will be calculated based on the users share of the main Reward token.

Using the Aludel v1.5 for example, we deposit into our Aludel every 14 days and have defined a release period of 1209600 seconds (14 days).

Example

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

## Configuration of an Aludel

### **Variables**

Staking Token (1) - This is the token you wish for users to 'lock' up to receive rewards, limited to ERC20, recommend to use LP tokens or similar for maximum benefit (LP farming) Reward Token (1) - This is the main token that you are rewarding to the user for locking the above token, this is the token that will be used for the main accounting. Bonus Token (0-50) - These are additional tokens that you wish to reward your users, these tokens will be available to the user based on the % of reward tokens the user is entitled to.

Multiplier: `Floor`, `Ceiling`, `Scaling Duration`

#### Example 1:

> Floor = 1
>
> Ceiling = 10
>
> Scaling duration = 60 days

For this configuration users will start at 1x (10%) and scale to the ceiling of 10x (100%) over 60 days.

#### Example 2:

> Floor = 1
>
> Ceiling = 3
>
> Scaling duration = 30 days

For this configuration users will start at 1x (33.33%) and scale to the ceiling of 3x (100%) over 30 days.

### **Funding Events**

Funding the reward program can be done in which ever strategy that you feel suits your requirements. There is a slow release mechanism that can be used to release tokens to users, over a set amount of seconds. Funding an aludel requires a smart contract call when the main `Reward Token` is being deposited. A `Bonus token` can be dropped directly into the Aludel pool without any contract call.

Using the Aludel v1.5 for example, we deposit into our Aludel every 14 days and have defined a release period of `1209600` seconds (14 days).

You can deposit as frequently as you like and set any release times that suits you, these durations can overlap and do not impact each other.

Some of our partners have expressed interest to deposit weekly into their reward programs so they can have a granular control over the rewards depending on the participation levels. If you wanted to do a large initial deposit as a one-off funding, that option is possible if you wanted to have a low maintenance approach.

If you decide to use a single large deposit with a long release period, please consider a larger multiplier scaling period. If you over-fund the program and wish to extract the tokens that were deposited the only way to do is by shutting down the whole contract (irreversible) - so users who haven't claimed before the shutdown will lose their rewards. (You can always announce a claim period and let users know if they pass the claim period they will forfeit their rewards).
