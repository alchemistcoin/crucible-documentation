# Introduction

Crucible in simple terms, is a smart wallet/vault that allows users to keep custody of their staked tokens.

Staked tokens get deposited into the users Crucible contract, and the vault/lock mechanism aspect is interacted by the reward program contract when a user subscribes to a reward program.

When a user subscribes to a program, their staking tokens are locked and cannot be removed from their Crucible but the user will be able to move their Crucible between their wallets or other even sell their positions (Crucibles can hold many different stakes and even just normal ERC20s).

If the user wants to remove their staked tokens, they will have to interact with the reward program and unsubscribe first.

As the locking functionality is local to the users Crucible, there are also opportunities of more capital efficiency by allowing multiple levels of locking on a single token balance if a protocol wanted to utilise that, such as multiple reward programs from the same project.

[It also has some highly detailed, dynamic artwork](../guides/artwork-of-the-crucible.md) which evolves based on the users reward program activity/participation

You can view artwork of other users Crucibles via [https://crucible.wtf/explore](https://crucible.wtf/explore).
