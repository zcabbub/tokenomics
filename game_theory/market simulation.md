

how do you create a market for an asset that has unlimited volume?


### actors functions: 
##### *objective*:
```ad-note
title: def
collapse: closed

obj func defines how are they trying to achieve the goal(*defined by utility function*)
```
- ***seller***: provide highest quality data
- ***buyer***: get highest quality data

#### *utility*:
```ad-note
title: def
collapse: closed

utility func defines what are they trying to achieve 
```
- ***seller***:
	- make a revenue
	- reinvest in another dataset
- ***buyer***: 
	- use quality data 
	- make a revenue


### Versions:
- [ ] 1 seller - N buyers
- [ ] N sellers - N buyers


#### grid interpretation:
- *different colors*: different actors
- *empty space*: available opportunity limited by discoverability
- *distance*: the closer you are to a seller, the better the price
- *movement*: 
	- ***why do they move?*** objective function optimization
	- doing a grid search to find the best offers from set
- *sellers lives*: the limited time opportunity 


#### Systems
***Bounty + Label + Pricing Engine: Dataset production system***
- system that produces random quality datasets to pe inputted in the ecosystem and issues a price for them 
- datasets are different based on Bounty 
- datasets have *different quality* based on Label 
- datasets have *different prices* based on Pricing Engine
- every X steps, the system produces new datasets
- CHANGE no. of datasets produced = no. of sellers
- the *mean* quality of the datasets increases with each production

***Local radial system***
- each seller is like a hot spot
- the price a buyer gets for the data is proportional with the distance to the seller? *- i.e. if you are X cells away from the seller your price is the dataset price multiplied with a factor derived from X*
	- Question: because we have a different price for each buyer, since datatokens change in value? 
- the closer you are to the center, the better the price/quality you have 
- the buyer can buy from everyone, but they choose to buy at the price he has now, or go 1 more step closer to it
	- the risk is the seller dying 


#### How the game works?

*Initial game setting*:
- **number of sellers, buyers** is set 
- **sellers and buyers lives** are set
- implicitly, **number of empty cells** is set
- first data products are issued (**Bounty**) and their quality is set randomly (**Label**), but increases over time
- * set buyers data *product* stock to 0 and sellers *product* stock to 1(since they receive initial data from Bounty-Label)
- sellers positions are **fixed** 
- for each seller: 
	- set a local radial system with the center in seller's cell.
	- the local ecosystem are: *dataset quality* and *price*


***Rules*:**
- move 1 step at a time
- when agents buy a product, the price changes
- buyers are satisfied with:
	- buying data the same quality they have
	- buying data of higher quality they have
- **agent cycle**: 
	- after X steps:
	1. some sellers disappear
	2. the buyers that became sellers get set and are the new sellers 
	3. new buyers are inputted


***For each step***:
- * check if any sellers are dying or not
	- if they are, a buyer with stock gets set and becomes seller
		- which buyer is chose?
		- what if none of the buyers have stock?
- buyers take 1 step towards the best new opportunity
	- *best new opportunity*:
		- product not already owned
		- same or better quality
	- **Question**: what the travelling means? i.e. it takes 2 steps to find a new opportunity? In system 2: the risk you take for the opportunity? you move closer, but the risk the seller to die
	- SYSTEM 1 - bonding curve?: 
		- are you on the seller's cell? buy from him.
		- you are still away? move. 
			- **Question**: What is the interpretation of the time spent moving there? on an online platform you have instant discoverability, i.e. you see all the sellers.
	- SYSTEM 2 - you can buy from everyone from everywhere
		- buy now at the price proportional with your distance to the seller
		- wait 1 more round to get closer and get a better price, but risk losing the opportunity(seller could die)


#### Questions
- [ ] What should the shelling point be? what should they converge to? higher quality data?


- [ ] how many empty spaces for each 2-3-4 party system?
	try a range and see the best performance
- [ ] 4 party system with AMM: Market makers exist to increase and manipulate volume, but with data, we have unlimited volume for data. How should a market maker look like?


1. bonding vs. staking?
3. what are we actually trying to find out through this market simulation? the question we're trying to respond
	1. we have multiple pricing systems. which one is the best to get the market in the least number of steps from valuation A to B?
3. **metrics to follow:**
	1. *fairness = price/quality ratio*: if we can maintain a fair marketplace? 
		1. check if it will increase? seems logical that the overall data price and quality will increase if the buyers have a rule to look for the best dataset. Maybe they should be limited to a radius?
	2. *max/min price*
	3. *max/min quality*
	4. evolution of the number or buyers and sellers
 


6. DONE what is the big grid axis?
	1. there is no grid, no visual convergence
	2.  just monitor that the price increases as the data quality and quantity increases



#### System 1 rules:
- buyers can only buy if they are on the same cell as sellers
- the price difference comes from the different time agents arrive to the seller
	- the later you come, the more money you pay

#### System 2 rules - :
- buyers can buy from everywhere, and their payment is proportional with the distance



Steps for experiments:
1. start with 1 product marketplace (much like oil)
	-  buyer, seller
	- metrics: bid ask spread
	- discoverability implies reducing bid-ask spread the dif between Ps - Pb
	- the quality is the same (NO curator)
2. add variable quality but still no curators
	1. matching based on best quality 
		1. 
	2. matching based on best quality at a desired price
		1. input order
	3. price range slippae
		1. ie accept a diff range of price offers
3. add the curators 
	1. di



