---
title: "Bug Bounty Program"
image: "/images/2020-landscape-2.png"
# meta description
description: "About the Filecoin Bug Bounty Program"
# save as draft
draft: false
submissions:
  - date: July 2020
    desc: "[Wei Yang](https://github.com/waynewyang) found a bug in `ConsensusFaultTimeOffsetMining` that could lead to incorrectly declared faults."
    mitigation: https://github.com/filecoin-project/lotus/pull/1988
  - date: July 2020
    desc: "[Wei Yang](https://github.com/waynewyang) found an issue with the `ReportConsensusFault` function caused it to not take effect."
    mitigation: https://github.com/filecoin-project/lotus/issues/1981
  - date: May 2020
    desc: "[Leo Zhang](https://github.com/Leozhang404) found that a message that could make the global cron actor's `HandleProvingPeriod` method crash."
    mitigation: https://github.com/filecoin-project/specs-actors/pull/383
---

<h4 class="has-text-align-center">Recent Submissions</h4>

{{< submissions >}}

#### Rewards

Reported security vulnerabilities will be eligible for a Bug Bounty based on Severity, calculated based on its Impact and Likelihood using the [OWASP Risk Rating model](https://owasp.org/www-community/OWASP_Risk_Rating_Methodology).

The following point ranges will be assigned based on Severity:

  - Critical: up to 25,000 points
  - High: up to 15,000 points
  - Medium: up to 10,000 points
  - Low: up to 2,000 points
  - Note: up to 500 points

Where currently 1 point = 1 USD (payable in USD, DAI or FIL).

Higher rewards will also be paid to reported vulnerabilities that offer quality written descriptions, test code, scripts and detailed instructions, and well-documented fixes.

Evaluation of the significance of the vulnerability and specific bounty amount assigned is at the sole discretion of the Filecoin Security Team, which consists of core developers and contributors.


> <small>NOTE: Reporters are responsible for all taxes and all awards subject to applicable law.</small>
> <small>We are not able to pay bounty awards to individuals who are on a U.S. sanctions list or in a country on a U.S. sanctions list..</small>

#### Rules

We encourage good-faith security research and ask that you follow these guidelines to avoid any confusion between legitimate research and malicious attack, we ask that you attempt, in good faith, to comply with the following:

- Testing must not violate any law or compromise any data that is not yours
  
- **Please refrain from the following**:
  - Denial of Service attacks and Active Exploits against the Filecoin network or Filecoin miners and nodes
  - Social engineering and phishing of Filecoin project contributors, ecosystem collaborators or community members
  - Physical or electronic attempts to access offices where project contributors work or data centers where Filecoin nodes are located
  - Compromising user accounts or stealing funds

<br>

- Please report any vulnerability you’ve discovered promptly.

- Help us improve this security process as it is critical to our mission by suggesting improvements

- Avoid violating the privacy of Filecoin users and community members, disrupting their systems, destroying data, stealing funds and/or harming the user experience

- Perform testing only on in-scope systems, and respect systems and activities which are out-of-scope

- Interact only with test accounts you own or with explicit permission from the account holder

- If a vulnerability provides unintended access to data: Limit the amount of data you access to the minimum required for effectively demonstrating a Proof of Concept; and cease testing and submit a report immediately

- Play by the rules. This includes following this policy as well as any other relevant agreements

- Use only Official Channels (emailing security@filecoin.org or Keybase chat) to discuss vulnerability information with us

- Handle the confidentiality of details of any discovered vulnerabilities according to our [Disclosure Policy](../security/disclosure-policy)


#### Scope

In scope for our Bug Bounty program are vulnerabilities in the core protocol and protocol implementations that have been security audited:

- Lotus Core
  - [filecoin-project/lotus](https://github.com/filecoin-project/lotus)
- Markets
  - [filecoin-project/go-fil-markets](https://github.com/filecoin-project/go-fil-markets)
  - [ipfs/go-graphsync](https://github.com/ipfs/go-graphsync)
- Storage Miner
  - [filecoin-project/lotus/tree/master/miner](https://github.com/filecoin-project/lotus/tree/master/miner)
- Actors
  - [filecoin-project/specs-actors](https://github.com/filecoin-project/specs-actors)
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

Visit the <a href="https://spec.filecoin.io/#intro__implementations-status" target="_blank">Filecoin Spec: Implementation Status</a> for more information about these projects and their audits.


#### Out-of-Scope

 - Filecoin websites and Filecoin infrastructure in general are not part of the bug bounty program.

 - Third-party services and websites that show information about the Filecoin network (block explorers, stats dashboards, price indicators, miner leaderboards, etc.) are also out of scope.

 - Vulnerabilities previously submitted by another person or identified in a published audit report are not eligible for bug bounty rewards.

 - Public disclosure of a vulnerability makes it ineligible for a bug bounty.

 Filecoin’s core development team, employees of Protocol Labs, the Filecoin Foundation and others paid by these organizations to work on the Filecoin project, indirectly or directly, are not eligible for bug bounty rewards.
