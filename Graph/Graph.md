                                                                                          https://thegraph.com/docs/en/


### Tasks
- better formalize incentives



### What is the Graph?
- an indexing protocol
- can build and publish open APIs, called subgraphs
		- making data easily accessible


#### Products
- **Graph Explorer**: Global GraphQL API
		- *explore subgraphs and interact with the protocol*
- **Subgraph Studio**
		- *create, manage, and publish subgraphs and API keys*
- **Hosted Service**
		- *create and explore subgraphs on the Hosted Service* 


#### Roles
- ##### Developer (/consumer?)
		- create subgraphs
		- use subgraphs with the API in dapps
	- *Incentives*:
			- *get indexed on Graph and advertised in Graph Explore*

```ad-danger 
title: Find more Incentives for developers
```
- ##### Indexer
		- operate a node to index data 
		- select subgraphs to index based on the subgraph’s **curation** signal
		- provide query processing services
		- GRT staked is subject to a thawing period and can be slashed if Indexers are malicious and serve incorrect data to applications or if they index incorrectly
		- consumers(e.g. apps) can set parameters for which Indexers process queries for their subgraphs
	- *Incentives*:
			- *earn query fees and indexing rewards for their services*
			- *Rebate Pool*
			- *earn rewards for delegated stake from Delegators, as a "tip" to contribute to the network*
- ##### [Curator](https://thegraph.com/docs/en/network/curating/)
		- organize data by signalling/*staking* on subgraphs
	- *Incentives*:
		- *rewards curators who signal on good quality subgraphs with a share of the query fees that subgraphs generate*
		- *are economically incentivized to signal early*
- ##### Delegator
		- network participants who delegate (i.e., "stake") GRT to one or more Indexers
		- contribute to securing the network without running a Graph Node themselves
	- *Incentives*:
		- *earn a portion of the Indexer's query fees and rewards*


```ad-question
title: network contributors=broad community? Everyone earns from the Rebate pool?
collapse: close
***Rebate pool***: all network contributors earn proportional to their work, following the Cobbs-Douglas Rebate Function
```

```ad-question
title: what is the Cobbs-Douglas rebate function?
collapse: close
```

```ad-question
title: How do they figure if the users are malicious and index incorrect data to applications or index incorrectly?
```