# The Cosmos Validators League.

In Cosmos and other PoS blockchains, validators play the critical role of signing transactions and securing the network. However, a major issue all networks have to deal with is the concentration of economic and voting power.

## Voting power issue.

In most Tendermint chains, a small group of validators hold a very significant portion of the supply. E.g the Cosmos Hub is one of the most decentralized chains of the network, yet only 15 validators hold over 51% of the total voting power.

Over time, that kind of skewed distribution will lead to the same oligarchic financial regime that we observe in traditional finance, and that crypto is supposed to fight against.

Last month on Terra, a small group of validators joined the Discord private group called “Terra Rebirth League” to coordinate a chain halt, disabling of staking and disabling of the market module in an attempt to prevent a governance attack following the excessively fast Luna fall.

The fact that the coordinated action of a small group of validators could have such a massive & instantaneous impact on investors is a serious warning sign that corrupting the network of a billions dollar chain like Terra isn’t completely out of the realm of possibilities.

Chains like Ethereum, who do enjoy a much higher validator count, are still being run by a limited number of powerful entities as they create multiple nodes and distribute coins across them to get around the network-imposed restrictions on centralization.

## Economic power issue

On the Cosmos Hub, the biggest validator has close to 500x more $ATOM than the smallest validator in the active set. That issue is consistent across most of the Cosmos chains.

It creates a situation where the top validators capture a very large portion of the block rewards while bottom validators barely break even. As a consequence, top validators are consistently increasing their control of the chain, while bottom validators are more likely to throw in the towel or fall out-of the active set, creating a vicious circle that exacerbates the issue.

## Root cause

We believe the root cause to be a lack of trust and awareness from the general public for smaller lesser-known validators. And sometimes for good reason, as we’ve seen recently with the Osmosis exploit by Firestake (former validator team).

The lack of trust is exacerbated by the impracticality associated with picking validators smaller validators within popular staking interfaces like the Keplr wallet ; since the default Keplr ranking is based on the number of coins delegated and presents the bigger validators first, it unintentionally prompts users to delegate to them.
https://wallet.keplr.app/#/cosmoshub/stake


## Proposed solution

We think the best way to solve it is to provide Cosmos delegators with an efficient way to voluntarily distribute their political & economic power across reputable community validators.

We’re setting out to build a new ranking that reflects more accurately the value each validator brings to the networks in which it participates. The value score will need to take into account both quantitative and qualitative metrics:

### <u>Quantitative metrics</u>

The following quantitative metrics will be taken into account:
<ul>
<li> Longevity
<li> Uptime
<li> Slashing events
<li> Number of relayed packets
<li> Vote participation
</ul>

### <u>Qualitative metrics</u>

We plan to integrate some qualitative data into the total score: sufficient information will be provided for each validator, and qualifying delegator wallet will be able to grade validators on-chain for the following criteria:
<ul>
<li>Contribution: Track record for contributions to the growth of the ecosystem through the technical expertise</li>
<li>Participation: Track record for participations in governance, e.g putting forward new proposals or reviewing,
voting & communicating proposals clearly to delegators</li>
<li>Alignment: Track record for good behavior & acting in the long term interest of the chain(s) being validated
</ul>

Some research will need to be performed to determine the conditions under which a wallet qualifies for voting and avoid abuse.


### <u>Listing requirements</u>

We will also be considering enforcing a basic "code of conduct" for validators that wish to be included in the community ranking, which would involve implementing good social & security practices (such as double-sign protection via TMKMS or Horcrux for instance)

### Features

The actual validator ranking is the core feature of the project.

Other potential features include:
<ul>
<li>Grade module for delegators to vote on-chain for their favorite validators
<li>History module to show how the score of each validator has changed over time
<li>Integration with the Restake app for automatic re-delegation to top ranking validators
<li>“Delegation score” per wallet, based on the ranking of the associated validators
</ul>

That delegation score is especially interesting as it would somewhat "gamify" the experience of promoting network decentralization. It could also be something that new Cosmos projects could take into account in their airdrop distributions, like @coslend & @CronusFinance are doing

In addition, we’re planning to allow multiple sorting options, e.g:
<ul>
<li>Sort by overall score
<li>Sort by qualitative / quantitative metrics only
<li>Sort by overall score weighted by delegation size
</ul>

The purpose of that option would be to display deserving “smaller” validators before the bigger ones, thereby encouraging a better distribution of delegations across the entire active set.

### Implementation
We’re planning the first version of the ranking and the grade module to be first accessible on the cosmosvalidators.org website.

However, the ranking data will be made fully available to third-party applications through a public API. These third-parties may include for example:
<ul>
<li>Ecostake’s <a href="https://cosmos.directory">Cosmos Directory</a> (which already provides the APIs and a simple user interface to surface on-chain information) and <a href="https://restake.app">Restake</a> app
<li>SparkIBC’s InterchainInfo website, which could also reward Spark point to users that decide to use the ranking for their delegations
<li>The awesome staking interfaces developed by Evmos & Omniflix
</ul>

The end goal for us would be to be integrated in Keplr or Cosmostation wallets as this is the primary way delegators
pick their validators.

<b>Another goal would be for the ranking to be taken into account:</b>
<ul>
<li>By the delegation programs of large coin holders like Ignite, Interchain Foundation, Informal, Osmosis Labs etc.
<li>By liquid staking protocols like Quicksilver, pStake, Lido, Shade Protocol etc.
</ul>

No shortage of use cases!

### Contributors
The project is currently being carried out by Thyborg, <a href="https://github.com/eco-stake">Ecostake</a> and <a href="https://github.com/gh0stdotexe">gh0st</a> from WhisperNode</a>. Based on community feedback, we might decide to formalize the “Cosmos Validator League'' as a DAO advocacy group to fund development and support its members.

We’re inviting all active community validators to join us, which can be done by contributing to the development effort, or simply participating in the new “Cosmos Validator League” Discord server to provide feedback on the ranking criteria, weights & parameters.
