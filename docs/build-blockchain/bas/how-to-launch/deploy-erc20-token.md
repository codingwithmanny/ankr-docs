---
title: Deploy ERC-20 Token
id: deploy-erc20-token
---

# Deploy ERC-20 token

Deployment of ERC-20 token can be done though Remix IDE of locally using truffle. 
Since BAS has EVM & Web3 support, it is compatible with Ethereum development toolsets. 
Remix is the easiest way to deploy the ERC-20 smart contract into a BAS network.

To deploy an ERC-20 token using Remix IDE go to the [remix page](https://remix.ethereum.org/). 
In the deploy section choose `Injected Web3` and make sure your MetaMask is connected to one of the BAS networks. 
To get connected to the BAS network, go to one of the BAS devnet's staking pages, for example, https://staking.dev-01.bas.ankr.com/, and it will create a new MetaMask network automatically for you. 
You can also configure your MetaMask manually.

Use this snippet of the ERC-20 smart contract:
```
// SPDX-License-Identifier: GPL-3.0
pragma solidity >=0.7.0 <0.9.0;

import "@openzeppelin/contracts/token/ERC20/ERC20.sol";

contract MyERC20Token is ERC20 {

    constructor() ERC20("My Test Token", "MTT") {
        _mint(msg.sender, 1000 ether);
    }
}
```

Now you can go to the `Solidity Compiler` section to compile your smart contract and deploy it to the BAS network via the `Deploy & Run Transaction` section.

:::warning
Make sure you choose `MyERC20Token` smart contract at the deployment stage.
:::