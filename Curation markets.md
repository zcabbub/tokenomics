#### *Def* [1]
- A curation market is a smart contract on Ethereum that is deployed for a specific shared goal or topic that allows the minting of tokens set by a hard-coded algorithm. 

- *Abstract definitions*: 
	- Curation markets allows groups to coordinate around shared goals (and interests) and benefit from the value they collectively create.
	- Curation markets leverage the wisdom of the crowd
- The main relation in a curation market is its [[Bonding curve|bonding curve]] [2]

##### Representation
- Rules for value tokenization are implemented in a smart contract that acts as a [[Terms#^d89a6d|schelling point]] for coordination.
- built on Ethereum
```ad-faq
title: works only on ethereum?
collapse: closed
```

#### Problems solved [1]
- Inability of extracting collectively created value
- Difficult coordination in unstructured groups
- Increasingly abundance of novel information

#### Core characteristics [3]
- A token that can be minted at any time (continuous) according to a price set by the smart contract.
- This price gets more expensive as more tokens are in circulation. 
```ad-tip
title: Is it neccesary that the price gets more expensive as we add more tokens?
collapse: close 
Why I can't use a descending function like $\displaystyle\frac{1}{x}$  which will have: ^6df173
- expensive tokens at the beginning, but unlimited supply very cheap after a while
- incentive to buy since it will get more affordable the more you buy? ^60ee1b

**Answer**: Bonding curves can take whatever shape the creator wishes.

```

- The amount paid for the token is kept in a communal deposit.
- At any point in time, a token can be withdrawn (“burned”) from the active supply, and a proportional part of the communal deposit can be taken with. 
```ad-danger
title: There is an incentive for the early adopters to sell later instead of remaining in the community, in order to make a profit. 
collapse: close
either by:
- reselling tokens
- burning them
```
```ad-question
title: what amount do I get out of the community pool, if the token increases in value as time passes?
collapse: closed

```
- The tokens are used to bond it to curators per sub-topic, who then curate information with their proportional backing.





#### *References*

[1] - de la Rouviere, S., 2017. *Curation markets* [online] 
Available at: https://docs.google.com/document/d/1VNkBjjGhcZUV9CyC0ccWYbqeOoVKT2maqX0rK3yXB20/edit

[2] - https://blog.oceanprotocol.com/curated-proofs-markets-a-walk-through-of-oceans-core-token-mechanics-3d50851a8005

[3] - de la Rouviere, S., 2017. _Introducing Curation Markets: Trade Popularity of Memes & Information (with code)!_. [online] Medium. Available at: <https://medium.com/@simondlr/introducing-curation-markets-trade-popularity-of-memes-information-with-code-70bf6fed9881> . 

