### *Tasks*:
+ finish ocean paper
+ look into data purgatory
+ competitors: kylin, graph(useful and good design), uniswap


#### Actors identities

***First tier***
- **publisher**:
		1. click publish
		2. fills out metadata
		3. provide URL where the data can be found
			- the URL gets stored encrypted on-chain
			- it is decrypted only at datatoken consumption
			*Problem*: they do not manage data storage AT ALL
		4. fill out price information
			- fixed
			- dynamic (automatic): add liquidity as desired to be in line with their target price
		5. hit *publish*
			- deploy a datatoken contract
			- publish metadata *on-chain*
*Problem*: ?mitigate rug-pulling()
```ad-question
title: dynamic(automatic) price mechanism = custom bonding curve? 
collapse: close
Thinking about us having different bonding curve templates for datasets, from which users can choose. 
Maybe corresponding to different types of auctions (e.g. English or Dutch)

quadratic auctions based on q voting

```

- **data providers** (liquidity providers - LPs/stakers)
	- 
- **buyers**
	1. connects wallet
	2. they already have some OCEAN
	3. click 'buy'
	4. Metamask asks for confirmation to swap OCEAN tokens for  1.0 datatokens
	5. the swap happens *on-chain*
- **consumers**
	1. connects wallet
	2. go to the dataset page corresponding to the datatoken you own
	3. click 'Use'
		- downloaded dataset 
				- *Problem*: privacy
		- results of bringing compute-to-data
				- *Problem*: not done yet


```ad-question
title: why swap for 1.0 datatokens?
represents access to the dataset probably, but is fungible
```
```ad-tip
compute-to-data is a means of federated learning
```

- **developers**
	- *Tools*: 
		- interfaces for smart contracts
				- Ocean JS
				- Python libraries
		- support for on-chain operations:
				- Ocean Aquarius
					- support for *storing* data on chain
					- query metadata (has local cache)
	- *Functionalities*:
			- create a *data asset* containing: provision data service, *deploy datatoken contract*, add metadata, *mint datatokens*
			- create a *fixed price* market
			- buy datatokens
			- consume a data asset (use a datatoken)
	- Ways to create a **datamarket**
			- Fork Ocean market
			- build up using Ocean Tools

```ad-question
title: So developers do not have support for dynamic price mechanisms?
```
```ad-question
title: Ocean Aquarius probably takes care of on-chain encrypt/decrypt of metadata. But Local cache means?
```

- **3rd parties**:
	- independent third-party marketplace runners (e.g. Daimler)
			- *runs client-side in browser using Ocean JS library -> common  decentralized backend*

```ad-question
title: liquidity providers are the same as marketplace runners?
collapse: close
```



#### Actions
- publish data
- set price
- stake datatokens
- *discover data*: browsing, searching and filtering
- buy/sell data
- consume data


#### Market arhitechture
- ***Common* Decentralized Backend**
		- *Solidity code* running on *EVM* chain
		- Contains:
			- data NFT & datatoken 
			- pool contracts
			- on-chain metadata storage
- **Frontends**
	- community market
	- Independent(third party)

![[Pasted image 20220921143020.png]]


```ad-question
title: Incentive for broader community, just for being memebers? is this a demonstrated working incentive?
```

```ad-question
title: Don't even need an account to use Ocean marketplace? they can do KYC just with wallet connection?
```

```ad-tip
title: Idea: tokenize the datasets using ZKP instead of letting the users divide a dataset into multiple ones and publish more multiple datasets.
collapse: close

might be unnecessary, and everything that is unnecessary dissapears over time. might not be used
```




