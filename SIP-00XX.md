---
SIP: XX
Title: Origins Subprotocol Update
Author: Shebin John (@remedcu)
Status: Ready to vote
Track: Origins
Created: 2022-01-17
---

# SIP-00XX: Origins Subprotocol Update

## Introduction

At Origins, we always try to make the right move the first time around - however, we aren't perfect. With further discussion since the last SIP, amongst our community, trusted advisors, the Sovryn team, and some of our early backers, we have come up with updated token economics and plan to conduct our public sale - which will give the project the best chance at early, and long-term success.

The first thing we needed to look at was our Bonding Curve - which was designed to link the SOV and OG token prices, and for us, it was an 'experiment' to see what effect it would have. After a few months of deliberation, we now see that although this is a wanted feature of the origins project, it came at too high a cost to the project to implement.

## Why move from Bonding Curve Token to Fixed Supply?

### First - High Capital Requirements
The bonding curve model requires a larger capital raise than might be optimal at this time. Due to the nature of the bonding curve, the funds raised do not go towards the project treasury, but instead, go towards the creation of OG tokens. At the expected $30m valuation, this would require a large SOV raise in order to provide sufficient collateral for the OG mint. 

While this may be fine from a strictly arithmetic perspective, because OG tokens can be unbonded, the current perception is that this is a distinct token and so the large raise can limit the remaining appetite for OG in the market after the sale, especially in the short run. 

This perception problem is partly due to the relative immaturity of the bonding-curve UI, as described below.

Given current market conditions and the experimental nature of this mechanism, it seems preferable to pursue a less risky strategy of listing directly on the Sovryn AMM. 

### Second - Market Perception
The unfortunate fact in this market is that a successful launch can add a lot of weight to early project adoption - and a failed launch can significantly hinder this adoption. As a launchpad, our three main metrics of success are our community, our ability to get marketing reach, and our ability to execute on projects that wish to launch with us. Simplifying our go-to-market and making it more efficient and easy to understand will significantly improve points 1 and 2, which will enhance the launch success of Origins itself and subsequent launchpad projects.

### Third - UX
The UI to make use of the bonding curve + SOV-bonded governance is still immature, and this can lead to a bad user experience. So while SOV-bonded tokens could use this methodology for the future, it may be too soon to risk it for OG given the short time period, we have before launching. 

## The advantage for SOV token holders &amp; stakers

- Veto Governance power over the Origins Governance. (unchanged)
- Staking Reward from Origins Revenue. (unchanged)
- Token allocation for SOV Stakers through various reward programs. (improved)
- SOV Stakers who participate in Origins launches & Governance will be eligible for additional rewards (improved)

## Direct and Indirect Revenue from Origins to Sovryn
The 20% is the direct revenue to SOV Stakers distributed through the Staking Reward program, provided to the Sovryn Exchequer from the Origins Exchequer.

But, in addition to that, Sovryn Stakers will receive 8% of the total token supply of OG Tokens through the different reward programs. And the Sovryn Team will receive 1.3% of the total OG token supply, respectively. So, 9.3% of the total token supply will be provided to Sovryn, which will amount to a further 4.65% of the revenue from Origins.

Thus, in total, Sovryn will be receiving 24.65% of the revenue from Origins.

Also, as new projects are introduced in the RSK ecosystem, more tokens will be listed in the Sovryn AMM, thus making more trades, creating more revenue from AMM fees.

## Proposed Initial Origins Revenue Distribution
The revenue earned from Origins is proposed to be divided as below:

- 20% of the revenue goes to SOV Stakers through Staking Reward
- 10% of the revenue goes to buying OG from the AMM for Community Incentive Programs.
- 50% of the revenue goes to OG Stakers through Staking Reward (including Vesting)
- 20% of the revenue goes to OG Treasury

## Tokenomics
You can find the detailed version of this tokenomics [here](https://docs.google.com/spreadsheets/d/1inCVPXsv58ozO1D1RBvvnJgA6UgUWjNhtLp8H4j3hog/).

All the tokens have their vesting/locked schedule with unlocking & receiver party details.

### SOV Stakers
SOV Stakers who believe in the OG project and wish to support it now have a significantly better chance of rewards compared to the previously developed model. In addition to just giving a uniform drip of OG rewards to SOV Stakers, rewards will be given to SOV Stakers who also participate in the OG Launchpad. The percentage of supply for SOV Stakers is increased, meaning that SOV Stakers that are active participants in OG will now get access to greater rewards. This benefits OG and SOV mutually in several ways:

- Greater demand for SOV tokens and for SOV staking (to gain access to the new rewards)
- A more significant % of rewards to SOV Stakers that support the Origins Launchpad
- OG tokens are airdropped to active SOV Stakers.

For example - an SOV Staker contributing to an Origins sale with a $5,000 allocation will be eligible to receive about $500 back in OG tokens as rewards if 10% is the decided reward. Rewards will be based on the amount raised on the platform - a higher raise will have a higher reward pool. 

### Sovryn AMM
A part of the token supply will be used entirely for creating an AMM pool for OG in Sovryn. Any reward received as an LP reward with this amount will be used again to incentivize the same AMM pool.

### Pre Sale & Community Sale
As the Presale and community sales have been significantly reduced, we need to overcome the issue of people needing to rush to get into the sale. The Pre Sale & Community Sale will be a pool-based sale system to solve this. For example, if the amount to be raised is $10K, and a total of $20K was raised, everyone will be refunded half of their deposit, and everyone will get 50% of their token allocation on a pro-rata basis.

This ensures that all the people get an allocation, whether they were the first or the last. As well as allowing all participants to purchase at the same price. This helps the protocol as well to keep it as distributed as possible.

### Liquid Fund & Future Fund
A part of the token supply is divided into the Liquid Fund and Future Fund. Origins Treasury will handle the Liquid Fund, and the Future Fund will be used per Bitocracy for any future requirements deemed necessary by the community.

LP Rewards, Community Incentive Programs, Development, Ecosystem and Adoption needs, etc will be funded using the Liquid Fund for the foreseeable future.

## Token Sale

The Token Sale will occur in different rounds, with varying amounts of tokens and investment limits.

### Early Funders

The Early Funders token allocation is divided this way:

| Name | Party | Deposit | Token Amount | Price | Invest Limit | Total Raised | Vesting Period (Months) | Vesting Cliff (Months) |
| --- | --- | --- | --- | --- | --- | --- | --- | --- |
| Seed | Strategic Investor | Stable Coin | 15 Million | $0.2 | Min $50K | $3 Million | 16 | 3 |
| Presale | Sovryn Stakers | SOV | 4 Million | $0.25 | Max $5K | $1 Million | 14 | 2 |
|||||| **Total** | $4 Million |
|

This will, in total, raise $4 Million.

The SOV raised in the Early Funders round will be primarily used by Origins in Sovryn Bitocracy, allowing us to initiate SIPs under the Sovryn protocol. Any staking reward received from this will be used to support the OG AMM Pool in Sovryn.

The Stablecoin raised in the Early Funders round will be used by the Origins Treasury.

### Programmatic Sale

The Programmatic Sale token allocation is this way:

| Deposit | Token Amount | Price | Invest Limit | Total Raised | Vesting Period (Months) | Vesting Cliff (Months) |
| --- | --- | --- | --- | --- | --- | --- |
| RBTC | 5 Million | $0.4 | $10K | $2 Million | 12 | 1 |
|||| **Total** | $2 Million |
|

The RBTC raised by Programmatic Sale will be primarily used for the Origins Treasury and Sovryn AMM.

## Summary

The Bonding Curve is indeed a novel idea to move forward with a token structure, although we feel there are benefits to having it, at the moment the team understands that the benefits do not outweigh the costs to the project to implement it. As such we have updated our tokenomics and adjusted the amount we will raise from the pubic and SOV stakers, while also reducing the total supply to 75M tokens.

We have added an incentivization mechanism to reward SOV stakers who participate in Origins, meaning SOV stakers who believe in Origins will be rewarded on top of their SOV staking rewards.

In short, the mission for this SIP is to get approval for the changes to the Tokenomics and Revenue Distribution of Origins.

## Links

[Website](https://origins.xyz/)

[Twitter](https://twitter.com/OriginsXYZ)

[Instagram](https://www.instagram.com/originsxyz/)

[Linkedin](https://www.linkedin.com/company/originsxyz/)

[Reddit](https://www.reddit.com/r/OriginsXYZ/)

[Telegram ANN](https://t.me/OriginsANN)

[Discord](https://discord.gg/gjkPdRT9kA)