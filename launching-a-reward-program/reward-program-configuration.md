# Reward Program Configuration

### **Variables**

`Staking Token` (1) - This is the token you wish for users to 'lock' up to receive rewards, limited to ERC20, recommend to use LP tokens or similar for maximum benefit (LP farming)&#x20;

`Reward Token` (1) - This is the main token that you are rewarding to the user for locking the above token, this is the token that will be used for the main accounting.&#x20;

`Bonus Token` (0-50) - These are additional tokens that you wish to reward your users, these tokens will be available to the user based on the % of reward tokens the user is entitled to.

Multiplier: `Floor`, `Ceiling`, `Scaling Duration`

#### Multiplier Example 1:

> Floor = 1
>
> Ceiling = 10
>
> Scaling duration = 60 days

For this configuration users will start at 1x (10%) and scale to the ceiling of 10x (100%) over 60 days.

#### Multiplier Example 2:

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

### Simulation Sheet

We've put together a basic worksheet that will help you simulate a users stake within a reward program and the release of funds and multiplier during the programs existence.

[You can access the worksheet by clicking here](https://docs.google.com/spreadsheets/d/162ogkFVVzm29jzKAwVhVtX4fbnPoKjtmDZnjWVLGLlA/edit?usp=sharing)

We recommend that you make a copy of this sheet and then edit it to suit your current usecase.

