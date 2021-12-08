### REQUEST INFORMATION TO SUBMIT PROJECT ###
- Changed truffle.js to truffle-config.js to fix windows terminal problem
  as tiped here https://ethereum.stackexchange.com/questions/21017/truffle-microsoft-jscript-runtime-error

- Followed all tips in the link
  https://andresaaap.medium.com/architect-a-blockchain-supply-chain-solution-part-b-project-faq-udacity-blockchain-da86496fce55
  suggested in peer chat
  
## Part 1: Plan the project with write-ups ##
diagrams path : .\diagram in format jpeg or drawio
Activity
- activity_diagram_project3.jpg
- activity_diagram_project3.drawio
  ![Alt text](diagram/activity_diagram_project3.jpg)

Sequence (took from Part3 of Project's requirements)
- sequence_diagram_project3.png
 ![Alt text](diagram/sequence_diagram_project3.png)

State
- state_diagram_project3.jpg
- state_diagram_project3.drawio
 ![Alt text](diagram/state_diagram_project3.jpg)

Classes (Data Model)
- class_diagram_project3.jpg
- class_diagram_project3.drawio
 ![Alt text](diagram/class_diagram_project3.jpg)

## Part 2: Project write-up - Libraries ##
npm: 6.14.13

node: 14.17.3

truffle: 5.4.14 - a development framework for Ethereum

web3: ^1.6.1" - to connect on blockchain

Solidity: ^0.4.24 - to compile solidity language

@truffle/hdwallet-provider: ^1.7.0 - to manage connection to wallet from truffle

Infura - deploying smart contract

# Requirement 3: Project write-up - IPFS #
I didn't use IPFS

# Address Smart Contract Supply Chain #
SupplyChain.address : 0x131708b2ea909f5ca413c1c350a9fb06f6c47ab388fcddd932770853ebe92739

# ---------------------------------------------- #
# ---------------------------------------------- #
# ---------------------------------------------- #

TRUFFLE 

D:\blockchain\UdacityBlockchainDeveloper\Project3\project-6>truffle devel
Truffle Develop started at http://127.0.0.1:9545/

Accounts:
(0) 0x627306090abab3a6e1400e9345bc60c78a8bef57
(1) 0xf17f52151ebef6c7334fad080c5704d77216b732
(2) 0xc5fdf4076b8f3a5357c5e395ab970b5b54098fef
(3) 0x821aea9a577a9b44299b9c15c88cf3087f3b5544
(4) 0x0d1d4e623d10f9fba5db95830f7d3839406c6af2
(5) 0x2932b7a2355d6fecc4b5c0b6bd44cc31df247a2e
(6) 0x2191ef87e392377ec08e7c08eb105ef5448eced5
(7) 0x0f4f2ac550a1b4e2280d04c21cea7ebd822934b5
(8) 0x6330a553fc93768f612722bb8c2ec78ac90b3bbc
(9) 0x5aeda56215b167893e80b4fe645ba6d5bab767de

Private Keys:
(0) c87509a1c067bbde78beb793e6fa76530b6382a4c0241e5e4a9ec0a0f44dc0d3
(1) ae6ae8e5ccbfb04590405997ee2d52d2b330726137b875053c36d94e974d162f
(2) 0dbbe8e4ae425a6d2687f1a7e3ba17bc98c673636790f1b8ad91193c05875ef1
(3) c88b703fb08cbea894b6aeff5a544fb92e78a18e19814cd85da83b71f772aa6c
(4) 388c684f0ba1ef5017716adb5d21a053ea8e90277d0868337519f97bede61418
(5) 659cbb0e2411a44db63778987b1e22153c086a95eb6b18bdf89de078917abc63
(6) 82d052c865f5763aad42add438569276c00d3d88a2d062d36b2bae914d58b8c8
(7) aa3680d5d48a8283413f7a108367c7299ca73f553735860a87b08f39395618b7
(8) 0f62d96d6675f32685bbdb8ac13cda7c23436f63efbb9d07700d8669ff12b7c4
(9) 8d5366123cb560bb606379f90a0bfd4769eecc0557f1b362dcae9012b548b1e5

Mnemonic: candy maple cake sugar pudding cream honey rich smooth crumble sweet treat

⚠️  Important ⚠️  : This mnemonic was created for you by Truffle. It is not secure.
Ensure you do not use it on production blockchains, or else you risk losing funds.

truffle(develop)> test
Using network 'develop'.


Compiling your contracts...
===========================
> Everything is up to date, there is nothing to compile.

ganache-cli accounts used here...
Contract Owner: accounts[0]  0x7727F4462fe8B37aAf0FC333a9067B7C044C7E2b
Farmer: accounts[1]  0x7Ee91FCA921E213689d8948FcB142A37599D09A0
Distributor: accounts[2]  0xFbEF5F0F3E9BfedC0E014d502e203b118bF79af9
Retailer: accounts[3]  0x05Ea0912124ddDF0B4d3138567DC741e6895010c
Consumer: accounts[4]  0x7C1C44F89a047DBC1536cc6734D59b1514d2f10C


  Contract: SupplyChain
    ✓ Testing smart contract function harvestItem() that allows a farmer to harvest coffee (335ms)
    ✓ Testing smart contract function processItem() that allows a farmer to process coffee (192ms)
    ✓ Testing smart contract function packItem() that allows a farmer to pack coffee (186ms)
    ✓ Testing smart contract function sellItem() that allows a farmer to sell coffee (207ms)
    ✓ Testing smart contract function buyItem() that allows a distributor to buy coffee (212ms)
    ✓ Testing smart contract function shipItem() that allows a distributor to ship coffee (163ms)
    ✓ Testing smart contract function receiveItem() that allows a retailer to mark coffee received (261ms)
    ✓ Testing smart contract function purchaseItem() that allows a consumer to purchase coffee (255ms)
    ✓ Testing smart contract function fetchItemBufferOne() that allows anyone to fetch item details from blockchain (60ms)
    ✓ Testing smart contract function fetchItemBufferTwo() that allows anyone to fetch item details from blockchain (65ms)


  10 passing (2s)

- Fetching solc version list from solc-bin. Attempt #1

truffle(develop)> migrate --network rinkeby
Using network 'rinkeby'.

Running migration: 2_deploy_contracts.js
  Deploying FarmerRole...
  ... 0xc52551d432f0c602eed10626fa3d7485dca7034df94cbadb5c2dbf62e1a45c79
  FarmerRole: 0x6a24a094e44c3c88e1f291661f2f49e81b73fa8e
  Deploying DistributorRole...
  ... 0x888bdefc30383e39aa97313b2ed92f8b2695c473bf95b89233fe610b0008558a
  DistributorRole: 0xbc0891b2a1fb5aad8e261c2207b40c3f5894e848
  Deploying RetailerRole...
  ... 0xd08aab2cf1ac79de36bf1c263328631c40ba432e92a93709a0075b8f0ebb6fb0
  RetailerRole: 0xb2b7ab8e0b801e2522ae873027e7536a9eb34863
  Deploying ConsumerRole...
  ... 0x1730bdd7057a9fac980b13c15f8a0419f108c6bcdcfd795fb964c26c09e15120
  ConsumerRole: 0xb826dd5aeae10ad759edae996b69bdbb4c5d09fd
  Deploying SupplyChain...
  ... 0x9ff0b9225e5b47a5a702862019ae2c33dddf673175cfd8c582024468e2e63068
  SupplyChain: 0x1dbfe454580f0ed1a558475d149549f0447a87d8
Saving successful migration to network...
  ... 0x131708b2ea909f5ca413c1c350a9fb06f6c47ab388fcddd932770853ebe92739
Saving artifacts...