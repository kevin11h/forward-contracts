[![Build Status](https://travis-ci.com/WeTrustPlatform/forward-contracts.svg?token=52dbeJVrfqXvGhWfS1U6&branch=master)](https://travis-ci.com/WeTrustPlatform/forward-contracts)
# Forward Contracts

### Overview
Smart contracts to forward ETH to a pre-defined address.


### Requirements
- Accept incoming transactions from both normal and contract addresses. Be able to recieve any ETH/Tokens intentionally or unintentionally.
- Contract's balance (ETH and/or tokens) must be able to move to the pre-defined recipient i.e. we don't want money to be burned/stuck/lost in this contract in any cases.
- Contracts are pre-generated with Recipient's address being assigned in the constructor.
- Forwarding happens in a passive mode which requires a trigger to sweep the balance.
- Recipient can call other smart contracts via a proxy method. This is to recover ERC20 mistakenly sent to the Forward contract.
- Stateless, should not have any internal states except the recipient. In other words, it only serves one purpose which is forwarding the fund.


### Getting started
- `npm install`
- (Optional) Install ganache: `https://truffleframework.com/ganache`
- After sending ETH to the Forwarder contract, call `sweep` method to forward the balance to the pre-defined recipient 

### License
[GPL-3.0](https://www.gnu.org/licenses/gpl-3.0.txt) &copy; WeTrustPlatform
