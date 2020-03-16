Syscoin Core integration/staging tree
=====================================

[![Build Status](https://travis-ci.org/syscoin/syscoin.svg?branch=master)](https://travis-ci.org/syscoin/syscoin)

https://syscoin.org

What is Syscoin?
----------------

Syscoin is an experimental digital currency that enables instant payments to anyone, anywhere in the world. Syscoin uses peer-to-peer technology to operate with no central authority: managing transactions and issuing money are carried out collectively by the network. Syscoin Core is the name of open source software which enables the use of this currency.

For more information, as well as an immediately useable, binary version of the Syscoin Core software, see https://syscoin.org/, or read the [original whitepaper](https://syscoin.org/zdag_syscoin_whitepaper.pdf).

Syscoin is a merge-minable SHA256 coin which provides an array of useful services which leverage the bitcoin protocol and blockchain technology.

888 million total coins (deflation 5 percent per year, deflation on all payouts) Block time: 60 seconds target Rewards: 38.5 Syscoins per block deflated 5 percent per year. 10 percent to governance proposals 22.5 percent to miner 67.5 percent to masternode SHA256 Proof of Work Mineable either exclusively or via merge-mining any SHA256 PoW coin Masternode collateral requirement: 100000 Syscoins Masternode seniority: 35% increase after 1 year, 100% increase after 2.5 years Governance proposals payout schedule: every month There is a 5% deflation per year on Syscoin Governance funding per round (Approx. 2m Syscoins per month to start) Governance funding gets 5% deflation per round (superblock). See formula below. Consensus enforced segwit (all transactions have witness programs except coinbase) Codebase based off of latest Bitcoin Core (https://github.com/bitcoin/bitcoin) Services include:

Hybrid layer 2 PoW/PoS consensus with bonded validator system (masternodes) ZDAG technology for point-of-sale speeds and probabilistic confirmations useful for microtransactions Trustless sidechain access to Ethereum and back through a custom permissionless/trustless sidechain technology (SYSX bridge) https://github.com/syscoin/sysethereum Decentralized governance (blockchain pays for work via proposals and masternode votes) Digital asset creation and management. ZDAG is open-source and developed over the course of 12 months by [Blockchain Foundry Inc](https://www.blockchainfoundry.co/), with external audit done over 6 months by [Whiteblock](https://whiteblock.io). [Performance report can be found here](https://syscoin.org/tps_whiteblock_syscoin_report.pdf).

Governance formula: We have implemented a % decline schedule — starting the first month with 1500000 SYS and ending on the 24th month with 196708 SYS. After that period, the superblock starts with 151767 SYS a month and will decline 5% every year. Read more about it here: https://medium.com/@syscoin/syscoin-4-0-rewards-specifications-a3dc01d85adf.

Interoptibility through a trust-less, no custodian, no counterparty bridge to Ethereum. Existing ERC20 assets can move to and from Syscoin Platform Tokens at will. This is the first time a fractional supply, two-way bridge has been developed and brought to market. It will enable a scaling infrastructure for Ethereum as well as flexibility for existing Syscoin ecosystem. A sharing and collobrative approach to foster growth in the industry was the goal, this is the results of over 18 months of research and development by [Blockchain Foundry Inc](https://www.blockchainfoundry.co/). Documentation can be found [here](https://github.com/syscoin/sysethereum-docs)

For more information, as well as an immediately useable, binary version of
the Syscoin Core software, see https://syscoin.org/, or read the
[original whitepaper](https://syscoin.org/zdag_syscoin_whitepaper.pdf).

Syscoin is a merge-minable SHA256 coin which provides an array of useful services which leverage the bitcoin protocol and blockchain technology.

888 million total coins (deflation 5 percent per year, deflation on all payouts)
Block time: 60 seconds target
Rewards: 38.5 Syscoins per block deflated 5 percent per year.
10 percent to governance proposals
22.5 percent to miner
67.5 percent to masternode
SHA256 Proof of Work
Mineable either exclusively or via merge-mining any SHA256 PoW coin
Masternode collateral requirement: 100000 Syscoins
Masternode seniority: 35% increase after 1 year, 100% increase after 2.5 years
Governance proposals payout schedule: every month
There is a 5% deflation per year on Syscoin
Governance funding per round (Approx. 2m Syscoins per month to start)
Governance funding gets 5% deflation per round (superblock). See formula below.
Consensus enforced segwit (all transactions have witness programs except coinbase)
Codebase based off of latest Bitcoin Core (https://github.com/bitcoin/bitcoin)
Services include:

Hybrid layer 2 PoW/PoS consensus with bonded validator system (masternodes)
ZDAG technology for point-of-sale speeds and probabilistic confirmations useful for microtransactions
Trustless sidechain access to Ethereum and back through a custom permissionless/trustless sidechain technology (SYSX bridge) https://github.com/syscoin/sysethereum
Decentralized governance (blockchain pays for work via proposals and masternode votes)
Digital asset creation and management

Governance formula:
We have implemented a % decline schedule — starting the first month with 1500000 SYS and ending on the 24th month with 196708 SYS. After that period, the superblock starts with 151767 SYS a month and will decline 5% every year. Read more about it here: https://medium.com/@syscoin/syscoin-4-0-rewards-specifications-a3dc01d85adf

License
-------

Syscoin Core is released under the terms of the MIT license. See [COPYING](COPYING) for more
information or see https://opensource.org/licenses/MIT.

Development Process
-------------------

The `master` branch is regularly built and tested, but is not guaranteed to be
completely stable. [Tags](https://github.com/syscoin/syscoin/tags) are created
regularly to indicate new official, stable release versions of Syscoin Core.

The contribution workflow is described in [CONTRIBUTING.md](CONTRIBUTING.md)
and useful hints for developers can be found in [doc/developer-notes.md](doc/developer-notes.md).

Testing
-------

Testing and code review is the bottleneck for development; we get more pull
requests than we can review and test on short notice. Please be patient and help out by testing
other people's pull requests, and remember this is a security-critical project where any mistake might cost people
lots of money.

### Automated Testing

Developers are strongly encouraged to write [unit tests](src/test/README.md) for new code, and to
submit new unit tests for old code. Unit tests can be compiled and run
(assuming they weren't disabled in configure) with: `make check`. Further details on running
and extending unit tests can be found in [/src/test/README.md](/src/test/README.md).

There are also [regression and integration tests](/test), written
in Python, that are run automatically on the build server.
These tests can be run (if the [test dependencies](/test) are installed) with: `test/functional/test_runner.py`

The Travis CI system makes sure that every pull request is built for Windows, Linux, and macOS, and that unit/sanity tests are run automatically.

### Manual Quality Assurance (QA) Testing

Changes should be tested by somebody other than the developer who wrote the
code. This is especially important for large or high-risk changes. It is useful
to add a test plan to the pull request description if testing the changes is
not straightforward.

Translations
------------

Changes to translations as well as new translations can be submitted to
[Syscoin Core's Transifex page](https://www.transifex.com/syscoin/syscoin/).

Translations are periodically pulled from Transifex and merged into the git repository. See the
[translation process](doc/translation_process.md) for details on how this works.

**Important**: We do not accept translation changes as GitHub pull requests because the next
pull from Transifex would automatically overwrite them again.

Translators should also subscribe to the [mailing list](https://groups.google.com/forum/#!forum/syscoin-translators).
