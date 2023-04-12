Formalizing the problem:
- Environment
	- state - $O_t$ (observation) 
- Reward
	- signal per time-step
- Agent
	- state - $S_t$ (could be last observation - $S_t = O_t$ - or *complete history*, or a *generic update*)
	- policy - agent behaviour, *map between agent state to action*
		- deterministic policy: $A = \pi(S)$ - *for a particular state yield the same result always*
		- stochastic policy: $\pi(A|S) = p(A|S)$
	- value function - an estimation of future rewards, *expected return*
	- model - predicts what the environment will do next

Agent categories:
- value based
	- no policy
	- value function
- policy based
	- policy
	- no value function
- actor critic
	- policy
	- value function

Agent categories
- Model Free
	- Policy and/or Value function
	- no model (cannot predict the environment at all)
- model based
	- optionally policy and/or value function
	- model




Problems:
- not making profit. Do they have to?
- what contributes to the price discoverability of Data products? Show what can contribute


Assumptions:
- the agents valuations are maximum X far from real valuation
	- IDEA: you can show the difference in the profit of the agents when bidding strategies are more informed (tokenization -> more information embedded)
		- more informed -> agents' valuations are within 1 stddev from the real values
		- not so informed -> completely random, quantify the impact
- maximum item value is 60 = sum(10 * each of 6 qualities)
- all data is private(see below)


Questions:
- Discuss disutility from other collectors obtaining the same product (scarcity). 
	- different for public and private data
	- thesis: assume all data is private, define private (not publicly available)
- Model supply and demand: Data attributes (supply) and Participants Data Values (demand). Need a couple of attributes to set for the product and to randomize for the participants. 
	- consistency
	- completeness
	- timeliness
	- accuracy
	- privacy - personal data or not
	- variety - has outliers, how many categories (maybe is in consistency)

- competitive or truthful auction?
	- https://www.cs.cmu.edu/~sandholm/cs15-892F15/Competitive%20auctions%20for%20multiple%20digital%20goods.pdf
- multiple or single price auction?
	- single-price auction - using bids, determine the optimal price for everyone. ==Reduces the importance of specialized knowledge regarding market demand and production/collection== 
	- multi-price auction - using bids, determine the optimal price for everyone, but only those whose bid is not lower will pay it. 
		- to maximize seller's utility: *not sure*
		- to maximize buyer's utility: he can better display its needs
	- https://www.cs.jhu.edu/~scheideler/club/spring_02/p735-goldberg.pdf
- Initial price: 
	- if "VCG-digital goods" auction: how do I initialize the bids accordingly to their values? 
		- basically value-revealing, **truthful mechanism**. 
		- In a real setting you can count on the people's incentives to lower the price, but in a simulation?
		- *the same issue as we have with score-price translation.* 
	- if bonding curve: no bids, so from where do I start the bonding curve? 



components:
- valuation engine
- 




Economics Python - https://janboone.github.io/python_economics/economics.html 

#### Theoretical:
FAST solidity - https://learnxinyminutes.com/docs/solidity/


#### Practical:
Learn Web3 development
https://cadena.dev/
![[Pasted image 20230314020711.png]]
https://cryptodevhub.io/


https://buildspace.so/builds
Explore domains like web3, machine learning and artificial intelligence by building projects that just need a weekend.


Tokens:
- ERC1155 - https://docs.openzeppelin.com/contracts/3.x/erc1155#constructing_an_erc1155_token_contract


https://gist.github.com/hjpithadia/fff1e64668c9069a8caebd0ccdc49f04![[54ba43c5517fc66c57678d8fda98d7f6-c925fb2e629f01fa0c1b803b05ac525f4782f451.zip]]