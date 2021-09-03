---
SIP: N/A
Title: Add SOV as collateral for borrowing
Author: John Light (@john-light)
Status: Draft
Track: Parameter
Created: 2021-09-03
---

# SIP-X: Add SOV as collateral for borrowing

## Description

If approved, this proposal would enable SOV holders to use their SOV as collateral when borrowing using Sovryn.

## Motivation

Adding SOV as a collateral asset in the loan protocol would give SOV holders a way to gain liquidity from their SOV holdings without having to sell their SOV. A side effect of this is that it would enable SOV holders to go "leverage long" SOV by borrowing against their SOV collateral and using the proceeds of the loan to buy more SOV.

## Proposed change

Add SOV as collateral when borrowing, with the following parameters:
- SOV token contract address: `0xefc78fc7d48b64958315949279ba181c2114abbd`  
- Collateralization rate: 300%  
- Oracle: Sovryn SOV/RBTC AMM pool TWAP  

## License
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
