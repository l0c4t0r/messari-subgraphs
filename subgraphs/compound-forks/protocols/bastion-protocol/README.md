# Bastion Protocol Subgraph

## Calculation Methodology v1.0.0

### Total Value Locked (TVL) USD

Sum across all Pools:

`Pool Deposit TVL`

### Total Revenue USD

Sum across all Pools:

`(Pool Borrow Amount * Pool Borrow Rate)`

Note: This currently excludes Liquidations

### Protocol-Side Revenue USD

Portion of the Total Revenue allocated to the Protocol

Sum across all Pools:

`(Pool Oustanding Borrow Amount * Pool Borrow Rate) * (Pool Reserve Factor)`

Note: This currently excludes Liquidations

### Supply-Side Revenue USD

Portion of the Total Revenue allocated to the Supply-Side

Sum across all Pools

`(Pool Outstanding Borrows * Pool Borrow Rate) * (1 - Pool Reserve Factor)`

Note: This currently excludes Liquidations

### Total Unique Users

Count of Unique Addresses which have interacted with the protocol via any transaction

`Deposits`

`Withdrawals`

`Borrows`

`Liquidations`

`Repayments`

### Reward Token Emissions Amount

Amount of reward tokens (BSTN / wNEAR) distributed each day in a given market.

`rewardsPerSecond * 60 * 60 * 24`

### Protocol Controlled Value

Not applicable to Compound v2

### Outlier Events

- Bastion Protocol's USDT price oracle was artificially high for a period of two minutes resulting in a lot of liquidations. Our subgraph captures this behavior, but please note that the prices seem inflated due to the price oracle. We are not overriding the price it is returning.
  - Bastion's statement: https://bastionprotocol.medium.com/usdt-liquidation-incident-report-a33af2ab1de2

## Reference and Useful Links

Protocol: https://app.bastionprotocol.com/

Docs: https://bastionprotocol.gitbook.io/official/

Smart contracts: On chain

Deployed addresses: https://bastionprotocol.gitbook.io/official/technicals/contract-addresses
