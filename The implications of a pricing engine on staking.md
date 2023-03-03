#### How staking works with tokenized datasets? 

A data product is priced at *X* DATA tokens. The Data product contains 10 features.
People can stake *X* amount of DATA token into the data product pool to receive the ***whole*** dataset, with all the features  

#### How fractionary staking works? 

However, since we want to enable the liquidity-providing qualities of data tokenization, we have to offer ***fractionary ownership***.

Therefore, people must also be able to stake a proportional amount of DATA tokens, and get the respective proportional part of the data product. 
***Example***: if the respective person wants only 5 features, he should pay only 50% of *X* DATA tokens to own them. This is the naive approach.

We can augment it by taking advantage of the Data Pricing Engine. Considering that each feature has a weight provided, we can yield the final price as a combination of percentages and weights. ***Example***: if a person wants some specific 5 features he should pay 
(10% x W1 + 10% x W2 + ... + 10% x W5)  of X DATA tokens.
==*only post-Liquidity, since initially we want to provide opportunity through more asymmetries.*==

*However, this can only be achieved if  at the time of staking DATA tokens, we tax only on the Apparent value of the Data product, which is the **same for all** Buyers. 
Since the latent/extrinsic application-dependent value is **different** for each buyer, we have to tax it only at the time of use.

#### How do you extract value from the Latent value?

You simply tax only at the point of use, depending of the type of use. We can define standard fees for each Compute-to-Data or Data-to-Compute option. 
***Example:*** if some person owns part of a data product , after he staked X DATA tokens (*paid for apparent value*), he can provide more tokens depending on his type of application/use: replication, computations, etc. 


[[Topic of data as an apparent intrinsic quality]]


