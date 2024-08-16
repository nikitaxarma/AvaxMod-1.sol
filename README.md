# Overview
This project contains two Solidity smart contracts: an ERC20 token contract and a Vault contract. The ERC20 contract implements a basic token with minting and burning capabilities, while the Vault contract allows users to deposit and withdraw the ERC20 tokens, providing them with proportional shares in the vault.
# Setting Up Your EVM Subnet on Avalanche
1. Deploy your custom EVM subnet using the Avalanche CLI. Refer to the guide and Avalanche documentation for detailed instructions.
2. Define your native currency as an ERC20 token. This will be the in-game currency for your DeFi Kingdom clone.
3. Connect your EVM subnet to Metamask.
4. ```
   Network name : mynewSubnet
   New RPC URL : 
   http://127.0.0.1:9650/ext/bc/zHvrf7cCeiHrahC6Rz6rNuzuyWjWCX5UodMLCQwRJ1WzodJBy/rpc
   Chain ID : 12345567
   Currency symbol : MYSUBNET
   ```
# Deploying Smart Contracts
## Deployment
1. Deploy the ERC20 contract first.
2. Deploy the Vault contract with the address of the deployed ERC20 contract.
# Functions Explanation
## ERC20
1. transfer(address recipient, uint amount): Transfers amount tokens from the caller's account to the recipient account.
2. approve(address spender, uint amount): Approves the spender to spend amount tokens on behalf of the caller.
3. transferFrom(address sender, address recipient, uint amount): Transfers amount tokens from the sender account to the recipient account, using the allowance mechanism.
4. mint(uint amount): Mints amount new tokens and assigns them to the caller's account, increasing the total supply.
5. burn(uint amount): Burns amount tokens from the caller's account, decreasing the total supply.
# Vault Contract
The Vault contract interacts with the ERC20 token, allowing users to deposit tokens and receive shares in return. Users can also withdraw their tokens by burning their shares.
1. constructor(address _token): Initializes the contract by setting the ERC20 token address to interact with.
2. _mint(address _to, uint _shares): Mints _shares and assigns them to _to, increasing the total supply of shares.
3. _burn(address _from, uint _shares): Burns _shares from _from, decreasing the total supply of shares.
4. deposit(uint _amount): Deposits _amount of ERC20 tokens into the vault, minting corresponding shares for the caller.
5. withdraw(uint _shares): Withdraws the corresponding amount of ERC20 tokens by burning _shares from the caller.
# Testing Your Application
1. Use Remix to interact with the deployed smart contracts.
2. Test functions like minting, burning, depositing, and withdrawing to simulate in-game activities.
3. Confirm transactions on Metamask.
# License
This project is licensed under the MIT License. See the LICENSE file for details.
# Author
* Nikita Sharma
