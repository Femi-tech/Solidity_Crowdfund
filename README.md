# PupperCoin

![Crowdfund](./image/Crowdfund.jpg)

This contract provide you  a platform to raise fund by crowfinding on Ethereum platform. You can follow crowfinding procedure step by step as belowed. 

## Contracts

* PupperCoin.sol
* CrowdSale.sol

## Deploy Contracts

### 1. Mint your coin.

Use `PupperCoin.sol` to mint your coin on minter account setted in the contract. Use `Remix` to compile and deploy the contract by providing neccesary variables such as `name`, `symbol`, and `initial supply`. 

![construct1](./image/1_construct_puppercoin.png)

These are functions relevant to minting your coin.

![deploy1](./image/2_puppercoin_depolyed.png)

You can add minter account address by `addMinter`.

![minter](./image/3_add_minter_account.png)

Then mint the coin in `mint`.

![mint](./image/4_mint.png)

Don't forget to check balance in minther account by using `isMinter` and `balanceOf`.

![balance](./image/5_check_coin_details.png)

### 2. Crowdsale.

Now you can sell your coin to raising fund by deploying `CrowdSale.sol` contract. Use `Remix` to compile and deploy the contract by providing neccesary variables such as `rate`, `token address`, `wallet address`and `goal`.  

For `rate`, you can hardcode a rate of 1, to maintain parity with Ether units (1 TKN per Ether, or 1 TKNbit per wei). If you'd like to customize your crowdsale rate, follow the Crowdsale Rate calculator on OpenZeppelin's documentation. Essentially, a token (TKN) can be divided into TKNbits just like Ether can be divided into wei. When using a rate of 1, just like 1000000000000000000 wei is equal to 1 Ether, 1000000000000000000 TKNbits is equal to 1 TKN.

![construct2](./image/6_construct_crowdsale.png)

These are functions relevant to crowdsaling your coin.

![deploy2](./image/7_crowdsale_depolyed.png)
