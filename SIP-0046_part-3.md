---
SIP: '0046'
Title: Transferring ownership of Sovryn contracts (Part 3)
Author: cowsant (@cwsnt), John Light (@john-light), Ororo (@ororopickpocket)
Status: Draft
Track: Contract
Created: 2022-04-21
---

# SIP-0046: Transferring ownership of Sovryn contracts (Part 3)

## Description  

If approved, this proposal will result in an on-chain state change transferring the administrator role in the Sovryn AMM smart contracts from the Exchequer Multisig to the timelock contracts governed by SOV stakers. The exact transfer details are as follows:

| Contract name	        | New governor                                                 |
|:---------------------:|:------------------------------------------------------------:|
| SovrynSwapNetwork     | TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`) |
| SwapSettings          | TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`) |
| All converters        | TimelockOwner (`0x967c84b731679E36A344002b8E3CE50620A7F69f`) |
| All oracles           | TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`) |
| ContractRegistry      | TimelockOwner (`0x967c84b731679E36A344002b8E3CE50620A7F69f`) |
| ConverterFactory      | TimelockOwner (`0x967c84b731679E36A344002b8E3CE50620A7F69f`) |
| ConversionPathFinder  | TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`) |
| ConverterUpgrader     | TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`) |
| converterRegistryData | TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`) |
| oracleWhitelist       | TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`) |
| rbtcWrapperProxy      | TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`) |

Note that these transfers will need to be approved in four different SIP votes, of which this proposal is only one part. All four proposals will need to be approved to effectuate the above changes.

Furthermore, this proposal will result in a signal from SOV stakers that they are willing and ready to accept the owner and/or adminstrator role in the following Sovryn smart contracts, to be transferred by the Exchequer Multisig no later than `2023-10-31 23:59:59 UTC`:

|	Category   | Contract name	         | Role  | New governor                                                      |
| ---------- |:----------------------:|:-----:|:-----------------------------------------------------------------:|
| Core       |                        |       |                                                                   |
|            | Protocol               | Owner | TimelockOwner (`0x967c84b731679E36A344002b8E3CE50620A7F69f`)      |
|            |	Protocol               | Admin	| TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`)      |
| Connectors |                        |       |                                                                   |
|            | LoanTokenLogicBeacon   | Owner | TimelockOwner (`0x967c84b731679E36A344002b8E3CE50620A7F69f`)      |
|            |	LoanToken              | Owner | TimelockOwner (`0x967c84b731679E36A344002b8E3CE50620A7F69f`)      |
|            |	LoanToken              | Admin	| TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`)      |
| Governance |	                       |      	|                                                                   |
|            | Locked SOV             | Admin | TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`)      |
|            | Staking                | Admin | TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`)      |
|            |	StakingRewards         | Owner	| TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`)      |
|            | Vesting Registry       | Owner | TimelockOwner (`0x967c84b731679E36A344002b8E3CE50620A7F69f`)      |
|            | Vesting Registry       | Admin | TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`)      |
|            | Vesting Registry       | Admin | Exchequer Multisig (`0x924f5ad34698Fd20c90Fe5D5A8A0abd3b42dc711`) |
| Oracles    |	                       |      	|                                                                   |
|            |	BPro Price Feed        | Owner	| TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`)      |
|            |	MoC Price Feed         | Owner	| TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`)      |
|            |	RSK Price Feed         | Owner	| TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`)      |
|            |	Price Feeds Gateway    | Owner	| TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`)      |
|            |	PriceFeedV1PoolOracle  | Owner	| TimelockAdmin (`0x6c94c8aa97C08fC31fb06fbFDa90e1E09529FB13`)      |
| Other      |                        |       |                                                                   |
|            | Liquidity Mining       | Owner | TimelockOwner (`0x967c84b731679E36A344002b8E3CE50620A7F69f`)      |

## Motivation

Currently, all [upgradeable Sovryn smart contracts](https://docs.google.com/document/d/1gGY4Rua_FVBZCJCftzf14cD4c6kqg6VTr9g-9-uDCA0/edit), with the exception of Staking and FeeSharingProxy, are owned by the [Exchequer Multisig](https://github.com/DistributedCollective/SIPS/blob/main/SIP-0007.md) (not to be confused with the [Exchequer Committee](https://github.com/DistributedCollective/SIPS/blob/main/SIP-0041.md)). This ownership role gives the Exchequer Multisig the power to upgrade any of these smart contracts instantly, that is, with no time lock or advance notice. Similarly, the Exchequer Multisig currently also holds all administrator roles on Sovryn smart contracts, giving the Exchequer Multisig the ability to instantly change the modifiable parameters of these contracts.

This mode of operation has worked well enough for the project during its early stages, allowing the core team to respond quickly to issues, but as total value locked has increased, so too has the risk of maintaining this status quo.
 
## Proposed change

To mitigate risks to Exchequer Multisig keyholders and to the Sovryn protocol and its users, we propose transferring ownership and administration of all Sovryn contracts currently owned by the Exchequer Multisig to either the TimelockOwner or TimelockAdmin contract, as specified in the tables in the `Description` section above. This will put the contracts under the control of SOV stakers, increasing the decentralization and censorship resistance of these contracts. After the governor roles are transferred to SOV stakers, all proposed smart contract upgrades and parameter changes will have to go through a 24-hour voting period and up to 48-hour timelock, giving Sovryn stakers and users up to 72 hours to react to any changes they might disagree with.

Approval of this SIP will only result in the onchain transfer of the owner/administrator role in the AMM contracts. No SIP is needed to approve the transfer of governance roles in the other Sovryn contracts. However to ensure alignment with and readiness from SOV stakers, we are also asking in this proposal for SOV stakers to signal their willingness to accept governance responsibilities in all of the other Sovryn smart contracts too.

## Implementation

https://github.com/DistributedCollective/Sovryn-smart-contracts/pull/450

## License
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
