# Introduction

Ve(3,3) is the name for the protocol's mechanism of action and not the token's name. Ve(3,3) token's name is Solidly. Ve(3,3) is a combination of 2 mechanisms:

*   'Ve' mechanism (Vote Escrow): similar to Convex and Curve protocols.
*   Staking/Dilution (3,3): Olympus DAO.

It's a sophisticated tokenomics design that enhances long-term participation and aligns protocol incentives with fee generation. The model addresses issues in traditional liquidity mining by tying token emissions to fee generation and locking mechanisms. It uses dynamic emissions and NFT tokenization to create a sustainable and efficient DeFi ecosystem.

## Why ve(3,3)?

Ve (3,3) was created to fix issues seen in models like Curve Finance. The problem with those models is that users' money gets stuck (when it's locked in the LP) and can't move around easily, which lowers how effectively capital is used. Ve (3,3) aims to solve these problems and Andre thinks it'll revolutionize how tokens are made in the future.

## Key Mechanism
### Token Locking and veTokens

* ve`Token`s: Users lock base tokens (e.g., `$VELO` {velodrome-finance native token is `$VELO`}) to receive veTokens (e.g., `$veVELO`), which grant voting power and access to rewards.
* Lock Period: Ranges from 1 week to 4 years. Longer locks provide more voting power and rewards.
* Decay: veTokens decay over time, reducing voting power and rewards as the lock period progresses.

## Rewards

There are 3 forms of rewards in DeX(s) based on ve(3,3) protocol:
* Emissions
* Trading free
* Bribes

### Emissions

* Dynamic Emission Adjustment:
    * The protocol typically determines the number of tokens to be minted in the next epoch, for e.g.:
        * emissions with fixed decay rate.
        * emissions depending on the rate of circulating supply.
    * The allocation of these emissions to specific LPs is based on the proportion of votes each LP (gauge) receives.

    * Proportional Increase: veToken holders' balances increase proportionally with emissions to prevent dilution, this phenomenon is called rebasing {rebase}, basically adjusting the value of `token` so that the it's not affected by the inflation when new `token` is minted.

### Trading Fees

Trading fees originate from swap transactions associated with the Liquidity Pool. You can earn these fees by voting for any gauge you desire a share of. These fees are distributed at the beginning of each epoch. The rewards are provided in the same tokens as the LP-Tokens, for eg.

    * Rewards for LP with a pair of $BTC/$ETH will be in both $BTC and $ETH

### Bribes

Bribes are a form of supplementary incentives distributed by the protocol or partners (VCs), to the liquidity providers
    * You have the opportunity to vote and earn in any gauge that is currently offering bribes
    * Bribes are given out every epoch, just like other incentives.
    * Payment depends on the tokens offered as bribes in each gauge.

---

### NFT Integration

*    Tokenization: Lock positions are represented as NFTs, allowing trading and borrowing against locked tokens, adding liquidity.
*    Multiple Locks: Users can own multiple veNFTs, managing different lock periods and amounts.

### Fee Distribution

*    Protocol Fees: veToken holders earn fees generated by the protocol. Fees are typically distributed in the assets accrued, not the native token, to avoid correlation and volatility issues.

## Types of Liquidity Pools

* Volatile Pools

Volatile pools are defined as assets that have no direct correlation in price, examples are Chainlink `LINK` and Ethereum `ETH`. The price of `ETH` has no relation to the price of `LINK`.

Volatiles pairs use the following formula to determine the price:

`x × y ≥ k`

* Stable Pools

Stable pools are defined as assets that have a direct correlation to each other. Examples are USDC/USDT, wBTC/multiBTC, frxETH/wETH etc. The price of the 2 assets will trade very close to each other and thus a different approach can be taken to allow for much higher volume at low slippage.

Stable pairs use the following formula to determine the price:

`x³y + y³x ≥ k`

## Practical Applications
### Solidly’s Implementation

*    New AMM Design: Supports swaps between both correlated and uncorrelated assets, and integrates Uniswap v2 compatible interfaces.
*    Fee Incentives: Emphasizes trading fee generation over liquidity incentives. veSOLID holders earn fees and can receive bribes to vote for specific pools.
*    Initial Distribution: Tokens distributed based on voting weights, with an initial airdrop to top projects by TVL.

### Advantages and Disadvantages

#### Advantages:

*    Incentivizes Long-Term Participation: Encourages users to lock tokens, aligning interests with protocol longevity.
*    Sustainable Emissions: Adjustments ensure emissions do not lead to unsustainable inflation.
*    Capital Efficiency: NFT integration provides liquidity and secondary market trading options for locked tokens.

#### Disadvantages:

*    Complexity: Requires understanding of advanced tokenomics and game theory.
*    Liquidity Lockup: Locked tokens reduce immediate liquidity.
*    Potential Centralization: Large holders can exert significant influence over emissions and governance.