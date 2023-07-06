---
title: "Filecoin Bug Bounty Program"
image: "/images/2020-landscape-2.jpg"
description: "About the Filecoin Bug Bounty Program"
submissions:
  - date: Aug 2021
    desc: "[Joran](https://github.com/JoranHonig) reported arbitrary write vulnerability in go-ipfs."
    mitigation: https://github.com/ipfs/go-ipfs-files/pull/43
  - date: Sept 2021
    desc: "[Swapnil](https://in.linkedin.com/in/swapnil-kothawade-813854a7) reported Access Control Issues in Github Repository."
    mitigation: https://github.com/filecoin-project/merkletree/
  - date: Oct 2021
    desc: "[cryptowhizzard](https://github.com/cryptowhizzard) reported an Denial-Of-Service(DOS) vulnerability in Lotus."
    mitigation: https://github.com/filecoin-project/go-data-transfer/pull/271
  - date: Jan 2022
    desc: "[Brijesh](https://github.com/ethletic) reported an exposed Algolia API key in Github."
    mitigation: https://github.com/filecoin-project/retrieval-market-spec/commit/50387354c55f91d5c6dff5a898a4bebba9b3c434
---

#### Rewards

Reported security vulnerabilities will be eligible for a Bug Bounty based on Severity, calculated based on its Impact and Likelihood using the [OWASP Risk Rating model](https://owasp.org/www-community/OWASP_Risk_Rating_Methodology).

The following is a guide for how points may be allocated to issues reported based on severity:

  - Critical: up to 500,000 points
  - High: up to 100,000 points
  - Medium: up to 25,000 points
  - Low: up to 10,000 points
  - None: up to 5,000 points

Where currently 1 point = 1 USD (payable in USD, DAI or FIL).

Higher rewards will also be paid to reported vulnerabilities that offer quality written descriptions, test code, scripts and detailed instructions, and well-documented fixes.

Evaluation of the significance of the vulnerability and specific bounty amount assigned is at the sole discretion of the Filecoin Security Team, which consists of core developers and contributors.


> <small>NOTE: Reporters are responsible for all taxes and all awards subject to applicable law.</small>
> <small>We are not able to pay bounty awards to individuals who are on a U.S. sanctions list or in a country on a U.S. sanctions list.</small>


#### Scope (now includes reports for the FEVM implementation)

In scope for our Bug Bounty program are vulnerabilities in the core protocol and protocol implementations that have been security audited:

|Category      |Level   |Impact In Scope                                                                                                  |
|--------------|--------|--------------------------------------------------------------------------------------------------------|
|<div style="width:180px">**Blockchain/DLT**</div>|<div style="width:200px"><nobr>**Critical(POC required)**</nobr></div>|Network not being able to confirm new transactions (Total network shutdown)                             |
|              |        |Unintended permanent chain split requiring hard fork (Network partition requiring hard fork)            |
|              |        |Direct loss of funds                                                                                    |
|              |        |Permanent, repeatable freezing of funds affecting core protocol areas (fix requires hard fork)          |
|              |        |RPC API crash capable of impacting block production                                                     |
|              |        |Protocol-level bug causing breakage of all contracts deployed on the chain                              |
|              |        |Protocol-level bug that enables tricking contracts into sending funds to arbitrary addresses            |
|              |**High(POC required)**    |Unintended chain split (Network partition) with localized impacts                    |
|              |        |Transient consensus failures                                                                            |
|              |        |Inability to propagate new transactions                                                                 |
|              |        |Protocol-level bug preventing contracts from using their funds                                          | 
|              |        |Protocol-level bug causing the inability for developers to deploy new smart contracts                   |
|              |        |Protocol-level bug rendering a single contract unusable after the exploit (i.e. contract bricked)       |
|              |**Medium**  |High compute consumption by validator/mining nodes                                                  |
|              |        |Attacks against thin clients                                                                            |
|              |        |DoS of greater than 30% of validator or miner nodes and does not shut down the network                  |
|              |        |EVM instruction fails to execute, in a general way                                                      |
|              |        |Inability to deploy a contract under a specific circumstances                                           |
|              |**Low** |DoS of greater than 10% but less than 30% of validator or miner nodes and does not shut down the network|
|              |        |Underpricing transaction fees relative to computation time                                              |
|              |        |Contract on the platform fails to deliver promised returns, but doesn’t lose values                                              |
|              |        |EVM instruction fails to execute when provided with concrete parameters                                 |

- **Important notice for the issue criteria that is presented in the table:**
  - Security reports that are not explicitly listed in the table will still be reviewed and matched up against the severity classification based on their impact.

  <br>

- FVM
  - Reference FVM (ref-fvm)
    - Reference implementation of the Filecoin VM ([Repository](https://github.com/filecoin-project/ref-fvm)).
- Lotus Core
  - [filecoin-project/lotus](https://github.com/filecoin-project/lotus)
- Markets
  - [filecoin-project/boost](https://github.com/filecoin-project/boost)
  - [ipfs/go-graphsync](https://github.com/ipfs/go-graphsync)
- Storage Miner
  - [filecoin-project/lotus/tree/master/miner](https://github.com/filecoin-project/lotus/tree/master/miner)
- Actors
  - [filecoin-project/builtin-actors](https://github.com/filecoin-project/builtin-actors)
- Proofs
  - [filecoin-project/rust-fil-proofs-ffi](https://github.com/filecoin-project/rust-fil-proofs-ffi)
  - [filecoin-project/rust-filecoin-proofs-api](https://github.com/filecoin-project/rust-filecoin-proofs-api)
  - [filecoin-project/rust-fil-proofs](https://github.com/filecoin-project/rust-fil-proofs)
    - [filecoin-project/bellman/](https://github.com/filecoin-project/bellman/)
    - [filecoin-project/merkle_light](https://github.com/filecoin-project/merkle_light)
    - [filecoin-project/neptune](https://github.com/filecoin-project/neptune)
    - [filecoin-project/neptune-triton](https://github.com/filecoin-project/neptune-triton)
    - [filecoin-project/paired](https://github.com/filecoin-project/paired)
- Dependencies
  - [filecoin-project/go-address](https://github.com/filecoin-project/go-address)
  - [filecoin-project/go-amt-ipld](https://github.com/filecoin-project/go-amt-ipld)
  - [filecoin-project/go-bitfield](https://github.com/filecoin-project/go-bitfield)
  - [filecoin-project/go-cbor-util](https://github.com/filecoin-project/go-cbor-util)
  - [filecoin-project/go-crypto](https://github.com/filecoin-project/go-crypto)
  - [filecoin-project/go-data-transfer](https://github.com/filecoin-project/go-data-transfer)
  - [filecoin-project/go-fil-commcid](https://github.com/filecoin-project/go-fil-commcid)
  - [filecoin-project/go-padreader](https://github.com/filecoin-project/go-padreader)
  - [filecoin-project/go-sectorbuilder](https://github.com/filecoin-project/go-sectorbuilder)
  - [filecoin-project/go-statemachine](https://github.com/filecoin-project/go-statemachine)
  - [filecoin-project/go-statestore](https://github.com/filecoin-project/go-statestore)
  - [ipfs/go-hamt-ipld](https://github.com/ipfs/go-hamt-ipld)
  - [ipfs/go-ipld-cbor](https://github.com/ipfs/go-ipld-cbor)
  - [whyrusleeping/cbor-gen](https://github.com/whyrusleeping/cbor-gen)

<small>* Implementations undergoing active development that have not yet been security audited are currently not in scope.</small>

#### Read More

- Visit the <a href="https://spec.filecoin.io/#intro__implementations-status" target="_blank">Filecoin Spec: Implementation Status</a> for more information about these projects and their audits.

- [Filecoin Improvement Proposals(FIPs)](https://github.com/filecoin-project/FIPs/tree/master/FIPS)

#### Out-of-Scope

 - Filecoin websites and Filecoin infrastructure in general are not part of the bug bounty program.

 - Third-party services and websites that show information about the Filecoin network (block explorers, stats dashboards, price indicators, miner leaderboards, etc.) are also out of scope.

 - Vulnerabilities previously submitted by another person or identified in a published audit report are not eligible for bug bounty rewards.
 
 - Any smart contract deployed on the FVM platfom is not a part of the bug bounty program.

 - Public disclosure of a vulnerability makes it ineligible for a bug bounty.

 Filecoin’s core development team, employees of Protocol Labs, the Filecoin Foundation and others paid by these organizations to work on the Filecoin project, indirectly or directly, are not eligible for bug bounty rewards.
 


 #### Rules

We encourage good-faith security research and ask that you follow these guidelines to avoid any confusion between legitimate research and malicious attack, we ask that you attempt, in good faith, to comply with the following:



- Testing must not violate any law or compromise any data that is not yours

- **Please refrain from the following**:
  - Denial of Service attacks and Active Exploits against the Filecoin network or Filecoin miners and nodes
  - Social engineering and phishing of Filecoin project contributors, ecosystem collaborators or community members
  - Physical or electronic attempts to access offices where project contributors work or data centers where Filecoin nodes are located
  - Compromising user accounts or stealing funds

- Please report any vulnerability you’ve discovered promptly.

- Help us improve this security process as it is critical to our mission by suggesting improvements

- Avoid violating the privacy of Filecoin users and community members, disrupting their systems, destroying data, stealing funds and/or harming the user experience

- Perform testing only on in-scope systems, and respect systems and activities which are out-of-scope

- Interact only with test accounts you own or with explicit permission from the account holder

- If a vulnerability provides unintended access to data: Limit the amount of data you access to the minimum required for effectively demonstrating a Proof of Concept; and cease testing and submit a report immediately

- Play by the rules. This includes following this policy as well as any other relevant agreements

- Use only official channels (email security@filecoin.org or Keybase chat) to discuss vulnerability information with us

- Handle the confidentiality of details of any discovered vulnerabilities according to our [Disclosure Policy](../responsible-disclosure)


 <h4 class="has-text-align-center">Recent Submissions</h4>

 {{< submissions >}}

 #### Hall of Fame

 <details>
 <summary><strong><size="25px">2023</strong></summary>
 - <a href="https://www.twitter.com/m7mdharon" target="_blank">Mohamed Haroun</a>
 - <a href="https://www.linkedin.com/in/corriesloot" target="_blank">Corrie Sloot</a>
 - <a href="https://www.twitter.com/holybugx" target="_blank">HolyBugx</a>
 - <a href="https://twitter.com/milankatwal99" target="_blank">Milan Katawal</a>
 - <a href="https://www.linkedin.com/in/gaurav-bhatia-bb290916a/" target="_blank">Gaurav Bhatia</a>
 - <a href="https://www.linkedin.com/in/pratik-shetty-94460a1aa/" target="_blank">Pratik Shetty</a>
 - <a href="https://www.linkedin.com/in/krutikathakur/" target="_blank">Krutika Thakur</a>
 </details>

 <details>
 <summary><strong><size="25px">2022</strong></summary>

 - <a href="https://www.linkedin.com/in/swapnil-kothawade-813854a7/" target="_blank">Swapnil Kothawade</a>
 <br>
 - <a target="_blank" href="https://www.linkedin.com/in/anupam-singh-226463201/">Anumpam Singh</a>
 <br>
 - <a target="_blank" href="https://www.linkedin.com/in/beni-budiharto-815b8b86/">Beni Budiharto</a>
 </details>

 <details>
 <summary><strong>2021</strong></summary>

 - <a target="_blank" href="https://www.linkedin.com/in/raynaudoee/">Ezequiel Raynaudo</a><br>
 - Nishant Das<br>
 - cryptowhizzard<br>
 - ItsUnixIKnowThis<br>
 - <a target="_blank" href="https://www.linkedin.com/in/swapnil-kothawade-813854a7/">Swapnil Kothawade</a><br>
 - <a target="_blank" href="https://www.linkedin.com/in/joran-honig-180b78100/">Joran Honig</a><br>
 - Tin Tin<br>
 - robyhugeman<br>
 - yangming
 </details>

