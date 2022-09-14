# The Sovryn Improvement Proposal Process

**Version 0.2**

## RFC 2119 compliance
The key words "MUST", "MUST NOT", "REQUIRED", "SHALL", "SHALL NOT", "SHOULD", "SHOULD NOT", "RECOMMENDED",  "MAY", and "OPTIONAL" in this document are to be interpreted as described in [RFC 2119](https://tools.ietf.org/html/rfc2119).

## What is a Sovryn Improvement Proposal?
A Sovryn Improvement Proposal, or "SIP", is a document that details a change to the management, allocation, or use of shared resources owned or directly influenced by Sovryn. All SIPs SHOULD be consistent with the requirements outlined in this document. The SIP author is responsible for building consensus within the community for their SIP and documenting dissenting opinions.

## Purpose
The purpose of the Sovryn Improvement Proposal Process ("the SIP process") is to provide a structured process for making changes to the shared resources of Sovryn. For these shared resources, a governance process is needed to grant or deny access and approve or reject proposed changes. By creating a fair, lightweight, and transparent governance process, the authors of this process hope to give SOV holders a meaningful say in the governance of Sovryn and increase the chances of Sovryn's success.

## Proposal workflow
Parties directly involved in the process are the _SIP author(s)_ (you), _Sovryn Voters_, _Sovryn Guardians_, and _SIP Editors_. Each of these roles is explained later in this document.

Proposals SHOULD follow this workflow:

* Stage I: Select SIP Track  
* Stage II: Pre-proposal  
* Stage III: Draft Proposal  
* Stage IV: Review Periods  
* Stage V: Bitocracy Vote  

> A proposal is NOT REQUIRED to go through Stages I-IV before it is submitted for a Sovryn Vote in Stage V. However it is strongly RECOMMENDED to follow this whole process so that the proposal gets a proper review and is not perceived with suspicion or hostility by Sovryn Voters. If a proposal is urgent, it MAY go through an accelerated review process if needed; if you feel your proposal is urgent, to align expectations you SHOULD make this urgency and the reason for urgency known when you introduce your proposal to the community.

### Stage I: Select SIP Track
Before you spend time working on a proposal, you SHOULD make sure the proposal complies with this process and has a chance of passing review by your peers. Review the SIP tracks and their requirements, then select the track that you think is best for your proposal. If your proposal meets the requirements, it has a much greater chance of being approved by Sovryn Voters.

There are five tracks that a SIP can be categorized into. Select the one you think is best for your SIP:

* Contract: proposals for modifying the source code of one or more Sovryn smart contracts  
* Issuance: proposals for increasing the total supply of SOV using the SOV token contract  
* Parameter: proposals for modifying one or more parameters on one or more Sovry smart contracts  
* Proclamation: proposals for making a public statement on behalf of Sovryn  
* Treasury: proposals for transferring funds from the Sovryn Treasury  

A proposal may be categorized as “Other” until a new, appropriate track is approved as part of a Meta SIP.

Each track has its own requirements for SIPs as follows:

**Contract**  
Proposals made to the Contract track SHOULD change one or more of the Sovryn smart contracts. The proposal SHOULD link to the existing contract(s) to be modified and to the source code of the proposed contract modification(s). All Contract track proposals SHOULD include a link to a third party audit report of the specified modification(s).

* All code modifications and associated documentation introduced by a Contract track proposal SHOULD be published under an MIT license.

**Issuance**  
Proposals made to the Issuance track SHOULD be used to increase the total supply of SOV tokens.

* All code, documentation, and content funded by an Issuance track proposal SHOULD be released under one of the following appropriate licenses:  
  * Creative Commons Zero (CC-0)  
  * MIT  

**Parameter**  
Proposals made to the Parameter track SHOULD change one or more of the Sovryn smart contract parameters. The proposal SHOULD include information about both the current parameter (if any) and the proposed change to the parameter. All Parameter track proposals MAY include a link to an analysis of the specified parameter change(s).

* All parameter modifications and associated documentation introduced by a Parameter track proposal SHOULD be published under the same license as the smart contract on which the parameter is being modified.

**Proclamation**  
Proposals made to the Proclamation track SHOULD be used to make a statement on behalf of Sovryn and can say whatever the author(s) want.

* For example, a Proclamation can be used to signal the Sovryn community's support for or disapproval of a certain RSKIP.  

**Treasury**  
Proposals made to the Treasury track SHOULD affect the movement of assets held by the Sovryn Treasury.

* All code, documentation, and content funded by a Treasury track proposal SHOULD be released under one of the following appropriate licenses:  
  * Creative Commons Zero (CC-0)  
  * MIT  

### Stage II: Pre-proposal
During Stage II you SHOULD seek feedback on your SIP idea by sharing it with your peers in the Sovryn community and soliciting their feedback. Examples of appropriate venues to share your SIP idea include:

* The [#bitocracy channel](https://discord.gg/WApXyz4D5h) in the Sovryn Discord  
* The [SIP category](https://forum.sovryn.app/c/bitocracy/sip-sovryn-improvement-proposals/) in the Sovryn forum  
* The Issues section of the SIPs repo  

Be open-minded and respectful of all feedback you receive. Adjust your proposal to address legitimate concerns as they come up to increase the odds of your proposal passing review in later stages.

### Stage III: Draft
After you have asked the Sovryn community whether an idea has any chance of support, and you have received sufficient feedback to feel confident going forward, you SHOULD create a draft SIP as a draft pull request to the SIPs repo. Use a template from the Templates section below to ensure you are including all the necessary information. Draft SIP files submitted to GitHub SHOULD be located in the `SIPs` directory and given a temporary name e.g. `SIP.md`, which the SIP Editor will later assign an SIP number, and SHOULD comply with the requirements set forth below to maintain consistency between SIPs.

* A SIP MAY be drafted and submitted from anywhere. The SIPs repo is used only as a matter of convenience and to ease coordination between Sovryn contributors.

**Templates**  
Below is a list of SIP templates for each track. Copy the template for the track your SIP is in, fill it out, and submit the pull request with your SIP for review. Sections marked as “required” in the template MUST be completed. Note that all SIPs MUST be licensed CC-0.

* [Contract](/templates/contract_template.md)  
* [Issuance](/templates/issuance_template.md)  
* [Parameter](/templates/parameter_template.md)
* [Proclamation](/templates/proclamation_template.md)  
* [Treasury](/templates/treasury_template.md)  

### Stage IV: Review Periods
After a SIP has been submitted as a draft pull request to the SIPs repo, it SHOULD undergo three review periods:

1. A Community Review, which starts the moment that a proposal has been submitted to the SIPs repo and lasts for one calendar week.  
2. An Editor Review, which starts when the Community Review ends and lasts for an indefinite period of time.  
3. A Final Review, which starts when the Editor Review ends and lasts for one calendar week.  

**Community Review**  
During the Community Review period, the SIP author will have a chance to respond to feedback and make changes to their proposal based on the feedback they have received to increase the likelihood of the proposal passing.  

**Editor Review**  
At the end of the Community Review period, SIP Editors will perform their review of the proposal. The SIP author SHOULD incorporate any changes suggested by the SIP Editor to prepare the proposal for the Final Review. After a proposal is reviewed by SIP Editors, an SIP Editor will ask the author if the proposal is ready for the Final Review. If the SIP Editors do not receive a response from the SIP author then the SIP Editors may at their discretion either close the pull request or move the proposal on for a Final Review.

* If agreeable, an SIP Editor will assign the SIP a number (generally the number of the SIP pull request), change the status of the SIP pull request from "draft" to "ready", and move the SIP on for a Final Review.  
* Reasons for denying an SIP number and closing the pull request include the SIP being too unfocused, too broad, duplication of effort, being technically unsound, not providing proper motivation or addressing legitimate concerns by reviewers, or not in compliance with this process.  

**Final Review**

During the Final Review, the proposal SHOULD NOT be changed. This gives Sovryn Voters a chance to review the proposal in its final state before the SIP is voted on.

### Stage V: Bitocracy Vote

After a SIP has gone through its Final Review, a SIP Editor will add a "Ready to vote" tag to the pull request. At the soonest available opportunity, Sovryn Guardians will review proposals that have the "Ready to vote" tag and decide whether or not they will veto the proposal.

Once a proposal has been tagged "Ready to vote", the SIP author MAY submit the proposal to Bitocracy for a vote by Sovryn Voters. Anyone else MAY submit the proposal instead but they SHOULD make an effort to communicate with the SIP author first to make sure the proposal is ready to be submitted and will not be accidentally submitted multiple times.

The vote description submitted for a Sovryn Vote SHOULD include a link to the specific commit of the proposal being voted on as well as the SHA-256 hash of the raw text file of the proposal.

* Example vote description: `SIP-2: Issuance of cSOV to community members. Details: https://github.com/DistributedCollective/SIPS/blob/00979e4d3b36e18b05f8088607809d8de03e261c/SIP-0002.md (SHA-256: 322cace15ffca9111b5fe1f3ce96ab54302144122c928489813926d33e0270f5)`  

Regardless of the vote outcome, after a SIP has been voted on a link to the vote will be added to the SIP header and the "Ready to vote" label will be removed. If a SIP is rejected by Sovryn Voters, then the pull request will be closed. If a SIP is approved by Sovryn Voters, then the pull request will be merged.

## Roles in the SIP process

### SIP Editors
SIP Editors are appointed by the owner of the SIPs repo. If the owner of the SIPs repo becomes hostile or unresponsive toward contributors then a new repo can be set up with new SIP Editors, and proposal activity can continue there.

SIP Editors have two responsibilities:

* Review SIPs during the Editor Review and prepare them for the Final Review  
* Update the SIP status and merge or close its pull request depending on the Sovryn Vote outcome  

**Review proposals**  
SIP Editors SHOULD review proposals and request modifications to them based on formatting and legibility. SIP Editors MAY close SIP pull requests due to inactivity.

**Update the SIP status**  
From the Final Review until the end of the Sovryn Vote, SIP Editors SHOULD update the SIP pull request and any associated pull requests as specified throughout this document.  

### Sovryn Guardians
Sovryn Guardians are members of the Guardian Multisig, who are appointed by the founding Sovryn team to protect the protocol against malicious proposals. The Guardian Multisig has the exclusive authority to veto onchain proposals submitted to the Sovryn Governance contract.

### Sovryn Voters
Sovryn Voters are holders of the SOV token who have staked their SOV in the Sovryn Staking contract. The voting power of Sovryn Voters is determined by the number of SOV they have staked and the length of time their SOV is staked for. More information about how voting power is calculated can be found [here](https://wiki.sovryn.app/en/governance/about-sovryn-governance). Sovryn Voters can find more information about staking and how to vote on SIPs [here](https://wiki.sovryn.app/en/governance/staking-vesting-voting).  

## License
Copyright and related rights waived via [CC0](https://creativecommons.org/publicdomain/zero/1.0/).
