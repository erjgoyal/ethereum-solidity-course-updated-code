# Ethereum and Solidity: The Complete Developer's Guide (Community Contributed Code Updates)

**========= FOREWORD: Important Solidity compiler version note (MUST READ!!) =========**

Currently the latest version of Solidity is [0.6.3](https://solidity.readthedocs.io). This repo provides up-to-date Solidity (and other) code for the benefit of the students enrolling/enrolled in the udemy.com course [Ethereum and Solidity: The Complete Developer's Guide](https://www.udemy.com/course/ethereum-and-solidity-the-complete-developers-guide/) and to this end it achieves that goal, that is, _all of the updated Solidity code in this repo is fully compatible with version 0.5.0 and higher of Solidity_. However if you want to deploy these smart contracts to the Rinkeby Test Network and then work with them without issues, you will need to use ABI and Bytecodes generated by a `0.5.x` version of the Solidity compiler, e.g. `0.5.15`.

I learned this the hard way as I was compiling using the 0.6.0 compiler when I started this repo only to realise that although I had no issue working with the contracts after deploying them to Ganache CLI's local test blockchain, this was not the case after deploying the same compiled bytecodes to Rinkeby, specifically all method calls to the contracts were only returning empty results.

**========= END OF FOREWORD =========**

## Purpose of this Repo

Up-to-date Solidity/web3.js/React code for the udemy.com course [Ethereum and Solidity: The Complete Developer's Guide](https://www.udemy.com/course/ethereum-and-solidity-the-complete-developers-guide/).

## The Reason

Toward the end of 2019 I became very interested in entering the blockchain development space and so I embarked on a journey to learn as much as I can, as quickly as I can, within this ever-evolving tech space we refer to as _Blockchain_, and to be more specific, the **Ethereum ecosystem**. Of course, I quickly realised that the development tools and packages being used to build, develop and deploy dApps and tech within this ecosystem all share a common trend: **rapid change and evolution, often introducing breaking changes through iterations of their releases**.

I make heavy use of the online learning website [udemy.com](https://www.udemy.com/) and find it to be a great supplementary learning tool. So naturally I bought a few courses on Ethereum and Solidity. The problem is, each of these courses target outdated versions of [Solidity](https://solidity.readthedocs.io/), [web3.js](https://web3js.readthedocs.io/) and [Truffle](https://www.trufflesuite.com/) in their course lessons and code examples. In the course creators' defense, remember, this is rapidly evolving tech we're dealing with here and the respective effort required to keep their video course content up-to-date with current software releases can be rather challenging.

_And so, that's where I decided to lend a bit of a helping hand_.

## Let the Code speak

I figured that if I wanted the online courses I enrolled in to provide up-to-date code then **other developers also had to want this**. So, I decided to take action and just write the updated code myself, starting with the Udemy course _Ethereum and Solidity: The Complete Developer's Guide_, the one I found most enjoyable and acceptable so far.

## Repository structure

This repository was setup as a monorepo, so as to keep the updated versions of the isolated bits of the course's code and tests well organized all within a single repository.

### Smart Contracts

The smart contracts created in the course are:

- [The Inbox Contract](/inbox/contracts/Inbox.sol)
- [The Lottery Contract](/lottery/contracts/Lottery.sol)
- [The CampaignFactory and Campaign contracts](/kickstart/ethereum/contracts/Campaign.sol)

### Working with the latest React tooling

The course sections that cover building out a front-end application using React make use of outdated versions of _Create React App_ and _Next.js_.

For Create React App, the previous approach of installing `create-react-app` globally via `npm install -g create-react-app` is no longer the recommended approach. As such if you have already used this command and installed `create-react-app` globally then you should uninstall the package using `npm uninstall -g create-react-app`. To create a new React app you may now use one of the following methods to ensure that you always use the latest React version:

- **npx**: `npx create-react-app my-app`
- **npm**: `npm init react-app my-app`
- **Yarn**: `yarn create react-app my-app`

For more details on the above methods, see [https://github.com/facebook/create-react-app](https://github.com/facebook/create-react-app).

**For the CrowdCoin app install whatever version of Next.js is currently the latest version, not the outdated version shown in the course.**

### The lottery-react App

To create the `lottery-react` app I chose to use the yarn command option, as follows:

```bash
yarn create react-app lottery-react
```

- [Browse the lottery-react App code files](/lottery-react)
- [lottery-react App README](/lottery-react/project-readme/README.md)

### The Kickstart/CrowdCoin App

- [Browse the CrowdCoin app code files](/kickstart)
- [Live Demo of the app](https://kickstart.owanh.now.sh/)

## Acknowledgement

I would like to give credit to [Stephen Grider](https://www.udemy.com/user/sgslo/) for creating the [excellent course](https://www.udemy.com/course/ethereum-and-solidity-the-complete-developers-guide/) for which I created this repository as my own personal add-on. If any mistakes or errors are found within any of this repository's content they should be attributed to an oversight on my part, and in no part should be deemed any fault of the Udemy course author, Stephen Grider.
