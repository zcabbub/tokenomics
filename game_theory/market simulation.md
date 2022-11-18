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

obj func defines how are they trying to achieve the goal(*defined by utility function*)
```
- ***seller***:
	- make a revenue
	- reinvest in another dataset
- ***buyer***: 
	- use quality data 
	- make a revenue

#### objective function optimization

#### grid interpretation:
- *different colors*: different actors
- *empty space*: ?
- *distance*: the closer you are to a seller, the more you afford to buy its data.
- *movement*: 
	- radial discoverability
	- ***why do they move?*** objective function optimization
	- doing a grid search to find the best offers from set

#### How the game works?
- set sellers
	- number sellers and buyers are variables
- buyers do a grid search to find the best offers and position themselves as close as possible to the cheapest/best offers
- actors move when:
	- when a seller dissapears
	- a buyer has no tokens
	- a buyer had fullfilled his order
- divide data by quality: 
	- higher quality data is more expensive


#### Questions
- [ ] What should the shelling point be? what should they converge to? higher quality data?


- [ ] how many empty spaces for each 2-3-4 party system?
	try a range and see the best performance
- [ ] 4 party system with AMM: Market makers exist to increase and manipulate volume, but with data, we have unlimited volume for data. How should a market maker look like?

