
![Crowdfund](./image/Crowdfund.jpg)

## This contract provide you a platform to raise fund by crowfinding on Ethereum platform. You can follow crowfinding procedure step by step as belowed. 

You will need to create an ERC20 token that will be minted through a `Crowdsale` contract that you can leverage from the OpenZeppelin Solidity library.

This crowdsale contract will manage the entire process, allowing users to send ETH and get back PUP (PupperCoin).
This contract will mint the tokens automatically and distribute them to buyers in one transaction.

It will need to inherit `Crowdsale`, `CappedCrowdsale`, `TimedCrowdsale`, `RefundableCrowdsale`, and `MintedCrowdsale`.

You will conduct the crowdsale on the Kovan or Ropsten testnet in order to get a real-world pre-production test in.

## Contracts

Using Remix, create a file called `PupperCoin.sol` and create a standard `ERC20Mintable` token.

Create a new contract named `Crowdsale.sol`, and prepare it like a standard crowdsale.


### 1.1: ERC20 PupperCoin

Open the PupperCoin.sol file you created on remix

Using `ERC20Mintable` and `ERC20Detailed` contract, hardcoding `18` as the `decimals` parameter, and leaving the `initial_supply` parameter alone.

There is no need to hardcode the decimals, however since most use-cases match Ethereum's default, you may do so.

### 1.2: Crowdsale
Open the Crowdsale.sol file you created on remix

You will need to bootstrap the contract by inheriting the following OpenZeppelin contracts:

* `Crowdsale`

* `MintedCrowdsale`

* `CappedCrowdsale`

* `TimedCrowdsale`

* `RefundablePostDeliveryCrowdsale`

Providing parameters for all of the features of your crowdsale, such as the `name`, `symbol`, `wallet` for fundraising, `goal`, etc. Feel free to configure these parameters to your liking.


### 1.4:  Testing the Crowdsale

- Test the crowdsale by sending Ether to the crowdsale from a different account (**not** the same account that is raising funds).
  
- Then test the time functionality by replacing `now` with `fakenow`, and create a setter function to modify `fakenow` to whatever time you want to simulate. 

### 1.5: Deploying the Crowdsale

Deploy the crowdsale to the Kovan or Ropsten testnet, and store the deployed address for later. Switch MetaMask to your desired network, and use the `Deploy` tab in Remix to deploy your contracts. Take note of the total gas cost, and compare it to how costly it would be in reality. Since you are deploying to a network that you don't have control over, faucets will not likely give out 300 test Ether. You can simply reduce the goal when deploying to a testnet to an amount much smaller, like 10,000 wei.

#### 1.5.1: Deployment on Kovan testnet

Deploy the crowdsale to the Kovan or Ropsten testnet, and store the deployed address for later. Switch MetaMask to your desired network, and use the Deploy tab in Remix to deploy your contracts.


