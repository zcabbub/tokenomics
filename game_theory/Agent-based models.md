 
### mechanism types
##### - bonding:
	- all prices are determined and enforced using a function between supply(total number of tokens issued) and price that defines the bonding curve
##### - staking
	- 
	- people stake their stablecoins/fiat into the Valyu project, to have access to datatokens
	- slashing
#####  - reputation


questions
```ad-question
title: Is the market a zero sumn game?
collapse: closed

_Yes_, we define the stock market as a zero-sum game, both in the short and in the long term, although it technically is incorrect.



more: https://www.quantifiedstrategies.com/is-the-stock-market-a-zero-sum-game/
```


#### 1. One data product marketplace, untokenized datasets -> 1 asset

##### Agents
- *there are N agents of **each type: buyer and seller** 
- there is an order book 
- the orders are randomized and NOT sorted
	- since we want to simulate the semi-liquid and discovery-limited market that datasets need
- the buyer has to either buy or sell
*optional*: this number stays constant over time: some agents get fulfilled and disappear, while other new unsatisfied ones are created
we have orders


##### Actions - *objective functions*
*buyers*:
- accept order saw
- place buy order

*seller*:
- accept offer
- place Sell order

TODO: maybe change the actions to accept offer and place offer 


##### Rules - utility, *reward mechanism*
- cooperate, i.e. make trade = accept offers
- negociate again, i.e. remake offers


##### Payoff matrices 
- buyer matrix:

$\begin{matrix}   NA & acceptOffer & SellOrder  \\ acceptOffer & 0 & 0 \\ SellOrder & 0 & 0 \\    \end{matrix}$


- seller matrix:

$\begin{matrix}   NA & acceptOffer & BuyOrder  \\ acceptOffer & 0 & 0 \\ BuyOrder & 0 & 0 \\    \end{matrix}$



#### 2. One data product - N quality types, tokenazed datasets -> N assets

What agents?








#### Experiments
- V - Valyu token
- D - Datatoken

1. V - bonding curve ; D - fixed price
2. V - ; D






#### Questions:
- [x] create different types of agents in Mesa?
- [x] read best practices ([pag. 44 mesa docs])
- [ ] read useful snippets 
- [ ] read - has [Schelling point](http://nifty.stanford.edu/2014/mccown-schelling-model-segregation/) 
- [x] see Mesa's schelling point implementation example 
- [ ] Schelling point example explanation: https://towardsdatascience.com/introduction-to-mesa-agent-based-modeling-in-python-bcb0596e1c9a
- [ ] examples: https://github.com/projectmesa/mesa/tree/main/examples


Implementation:
- [ ] turn it into a CLI tool
- [ ] create a simple 2 party sytem buyer seller 
	- [ ] assume that buyers don t move or reverse
	- [ ] buyers = curators
- [ ] add curator
- [ ] add centralized party 
- [ ] radius is proportional with wealth
	- *might be a problem with really big differences*


