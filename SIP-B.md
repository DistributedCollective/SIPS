---
SIP: N/A
Title: Concentrating staking revenues
Author: John Light (@john-light)
Status: Draft
Track: Contract
Created: 2021-09-07
---

# SIP-B: Concentrating staking revenues

## Description

- Currently staking revenues are paid to all stakers, regardless of whether the stake is encumbered by a vesting contract or not.  
- This SIP will modify the Fee Proxy and Staking contracts so that staking revenue is only paid out to fully-vested stake.  
- "Fully-vested stake" is defined as staked SOV that is not encumbered by a vesting contract.  
- Staking revenues will be divided among fully-vested stake pro rata on a block-by-block basis according to the fully-vested stake's voting power.  

## Motivation

Stakers are currently being paid a pro-rata share of revenue on the basis of voting power derived from both stake that is fully-vested and stake that is still encumbered by a vesting contract. In discussing [SIP-0024](https://github.com/DistributedCollective/SIPS/blob/main/SIP-0024.md), members of the Sovryn community determined that this arrangement is incompatible with the intention of vesting contracts, which is to incrementally increase SOV ownership and economic power over time. We propose to extend the logic of SIP-0024, which only provides SOV staking rewards to fully-vested stakers, to all protocol revenues earned by stakers, making only fully-vested stake eligible to receive a pro rata share of revenues.

## License
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
