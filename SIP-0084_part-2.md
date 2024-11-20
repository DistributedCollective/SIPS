---
SIP: '0084'
Title: Deactivate Fallback Price Oracle Contract (Part2)
Author: Tyrone Johnson (@tjcloa)
Status: Ready for vote
Track: Contract
Created: 2024-11-20
---

# SIP-0084: Deactivate Fallback Price Oracle Contract (Part 2)

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

Note that this is Part 2 of a two-part SIP.  
Both proposals will need to be approved to effectuate the complete set of changes.  
The exact change details for this part are as follows.  

If approved, this SIP will upgrade the PriceFeed contract on Zero protocol and will replace the fallback oracle with the DummyFallbackOracle contract.      
The new logic of the PriceFeed contract will revert on stale price, removes restriction on adding a dummy oracle that returns stale price and adds a new function to replace the primary oracle and the fallback oracle separately.  


__Existing contracts__  
| Contract                               | Address                                    |
| -------------------------------------- | ------------------------------------------ |
| PriceFeed proxy                        | 0x6D1d9574d67e04cf35Fa1d916F763eDDae03b75d |
| PriceFeeds logic                       | 0x1281ECfe66c9fA632Df1eB1eC19405C3b1bbaAf0 |

__New contracts__  
| Contract                               | Address                                    |
| -------------------------------------- | ------------------------------------------ |
| PriceFeeds logic                       | 0x867303dfCd696BE516f9C4023525F1107d903356 | 
| DummyFallbackOracle                    | 0x16261C66D8D687600E5CbF7945986044A6569cBe | 


## License
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
