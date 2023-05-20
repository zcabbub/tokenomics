### What they wanted to do: [1]

In *traditional* curation markets, the main action for actors is **stake** and **unstake** as a *means of signaling*.

Ocean wants to *bind* these actions with *actual work* of making services available, in a token mechanic called **Curated Proofs Markets *(CPMs)*** 

CPMs conditions:
- Predicted popularity
		- stake 
- Proofed popularity: each use is verified using a **cryptographic proof**
		- provably serve it when requested

**Bottom line**: people earn tokens if they "bet" on a service and make it available. 

```ad-question
title: Does Ocean let the users take care of data delivery('serve it') and privacy preserving?
```

##### Two types of tokens:
- Ocean tokens (**Ọ**) that are:
		- main unit for buying and selling services
		- used as block rewards
		- *fixed supply*
- Drops (**Ḍ**): 
		- e.g. if a user cares about a service, they will stake O on dataset X to get drops ("DX")
		- are used to *measure stake in a given service*, *unstaking* and *block rewards*
		- they are the token inside each curation market, and a measure of user's attention (mirroring attention scarcity)
		- they are derivative tokens of Ocean tokens
		- *variable supply* - as people stake more O, the D supply increases
```ad-question
title: derivative tokens? 
collapse: closed

like gwei?
```

```ad-tip
Therefore, a user will not only own O in their crypto wallet, but also DX, DY, depending on the service they are staked into.
```


### Use cases example:
##### Making a service available
*Steps:*
1. Alice has dataset X
2. She claims copyright on dataset X and stakes an amount of 50 O for doing it. 
3. Ocean network now has a pointer to dataset X, that the user manages
4. Vetting: the network has **5 days** to investigate if the user does indeed have copyright on X
		- 2 other actors check
		- if 1 or more does not agree, each of them has to stake O in order to challenge Alice and figure who was right
```ad-danger
title: potential poor design
collapse: close

Does not take into account that people do not really care about using their own resources for the sake of correctness. 

They should have an economic incentive to solve copyright.

```
5. Curation market is initialized
	- User gets DX accordingly to the bonding curve graph, following the formula: $\displaystyle{x}DX = \frac{staked O}{rate \frac{O}{DX}}$ , with $x$ being the amount received.
	- DX token supply increases with ${x}$ amount and the price is modified accordingly
6. The dataset is now available for download
```ad-question
title: What is the continous formula for any bonding curve? 
collapse: closed

A Riemmann sum? or we just take the average price
also, see example from [1]
```


7. Another user (Bob) downloads this dataset for free
8. Alice receives a computed block reward, that is calculated using:
			$\displaystyle{x}O = \frac{stake DX}{difficulty}$
	- $difficulty$ is a measure of effort, the 'power' used to normalize individual contributions
	- block reward is proportional with the staking
```ad-warning
title: check ocean whitepaper about $difficulty$ formula
```

9. If Bob finds dataset X useful, he can stake his O in X in order to receive a certain amount of DX. As 
	- *for the sake of this example, consider that he does that*
10. Bob makes X available for download as he staked O into it and now owns DX.

```ad-question
title: How do you actually make a dataset available for downloading? 
collapse:close
```


12. Joe wants to download the dataset X and he makes a *request* to the Ocean network.
13. If there are multiple providers available (this case, Alice and Bob) one is chosen **randomly** by the network

```ad-danger
title: potential poor design
collapse: close

Are they random because they have the same stake of DX?

```

14. As more people download, the rewards are divided between the providers, proportionally with their stake (DX owned).
15. At some point, if they want to sell, the early adopters are more incentivized to sell since they will make a bigger profit than the late adopters, i.e., they paid more O per DX


```ad-question
title: Does Ocean offer custom bonding curves for any dataset/service?
collapse:closed
```

```ad-question
title: is the block reward bonding curve the same for all datasets? 
collapse: close
```

```ad-question
title: Is it logarithmic? since they "disburse supply over time to drive near-term growth and long-term sustenability"
collapse: close

```



Other use cases:
- leveraging marketplaces
- privacy-preserving compute



#### *References*

[1] - https://blog.oceanprotocol.com/curated-proofs-markets-a-walk-through-of-oceans-core-token-mechanics-3d50851a8005
