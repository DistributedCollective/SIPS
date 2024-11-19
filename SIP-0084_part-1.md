---
SIP: '0084'
Title: Deactivate Fallback Price Oracle Contract
Author: Tyrone Johnson (@tjcloa)
Status: Draft
Track: Contract
Created: 2024-11-20
---

# SIP-0084: Deactivation of the Fallback Price Oracle Contract (Part 1)

## Description  

The Sovryn Lending and Zero protocols currently use the Rootstock Oracle price feed on the RSK blockchain as a fallback price oracle for WRBTC in USD. 
This fallback oracle is triggered when the primary oracle returns a zero price.  

The proposed change is prompted by the upcoming discontinuation of support for the Rootstock Oracle. 
After extensive research and analysis, it has been decided to deactivate the fallback oracle rather than replace it with another one. 
The primary Money-on-Chain oracle, which is decentralized, has demonstrated robust fault tolerance and reliability.  

Additionally, the price feed contract logic has been updated to include a stale price parameter.  
This ensures that outdated prices are not used and transactions will revert.   
The proposed technical solution involves replacing the RSK oracle with a "dummy oracle" that always returns a zero price and marks it as stale.  
This approach provides flexibility to replace the fallback oracle with another reliable oracle compliant with the Chainlink interface if the community decides to do so in the future.  

## Proposed Changes  

If approved, this SIP will replace the WRBTC price oracle in the PriceFeeds contract used for the Lending protocol with the address of the new PriceFeedsMoC oracle contract that has the DummyFallbackOracle as the fallback price oracle.  


__Existing contracts__  
| Contract                               | Address                                    |
| -------------------------------------- | ------------------------------------------ |
| PriceFeedsMoC                          | 0x391fe8a92a7FC626A25F30E8c19B92bf8BE37FD3 |
| PriceFeeds                             | 0x437AC62769f386b2d238409B7f0a7596d36506e4 |

__New contracts__  
| Contract                               | Address                                    |
| -------------------------------------- | ------------------------------------------ |
| MoC Price Feed                         | [TBD]   | 
| Dummy Fallback Price Feed              | 0x16261C66D8D687600E5CbF7945986044A6569cBe | 


## License
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
