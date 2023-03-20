For a given strategy $\sigma$, the support of $\sigma$: $\mathcal{S}(\sigma)$ is the set of strategies for which $\sigma_i>0$:

$$ i \in \mathcal{S}(\sigma)\Leftrightarrow \sigma_i > 0 $$

For example:

-   If $\sigma=(1/3, 1/2, 0, 0, 1/6)$: $\mathcal{S}(\sigma)=\{1, 2, 5\}$
-   If $\sigma=(0, 0, 1, 0)$: $\mathcal{S}(\sigma)=\{3\}$



## Definition of nondegenerate games

A two player game is called nondegenerate if no mixed strategy of support size $k$ has more than $k$ pure best responses.


For example, the following game is degenerate:

$$ A = \begin{pmatrix} 1 & 1 & 0\\ 2 & 3 & 0 \end{pmatrix}\qquad B = \begin{pmatrix} 1/2 & -1 & -1/2\\ -1 & -1 & 2 \end{pmatrix} $$

Indeed, consider $\sigma_c=(0, 0, 1)$, we have $|\mathcal{S}(\sigma_c)|=1$ and:

$$ A\sigma_c^T = \begin{pmatrix} 0\\ 0 \end{pmatrix} $$

So the number of pure best responses to $\sigma_c$ is 2.

Thus the game considered is indeed degenerate.



```
In [3]:

    
A = np.array([[1, 1, 0], [2, 3, 0]])
sigma_c = np.array([0, 0, 1])
(np.dot(A, sigma_c))
```

```
    Out[3]:

array([0, 0])
```

## Support enumeration algorithm[](https://notebook.community/drvinceknight/gt/nbs/chapters/05-Support-enumeration#Support-enumeration-algorithm)

[Video](https://youtu.be/w5MDcvzNI_A?list=PLnC5h3PY-znxMsG0TRYGOyrnEO-QhVwLb)

For a nondegenerate 2 player game $(A, B)\in{\mathbb{R}^{m\times n}}^2$ the following algorithm returns all nash equilibria:

1.  For all $1\leq k\leq \min(m, n)$;
2.  For all pairs of support $(I, J)$ with $|I|=|J|=k$
3.  Solve the following equations (this ensures we have best responses):
    
    $$\sum_{i\in I}{\sigma_{r}}_iB_{ij}=v\text{ for all }j\in J$$
    
    $$\sum_{j\in J}A_{ij}{\sigma_{c}}_j=u\text{ for all }i\in I$$
4.  Solve
    -   $\sum_{i=1}^{m}{\sigma_{r}}_i=1$ and ${\sigma_{r}}_i\geq 0$ for all $i$
    -   $\sum_{j=1}^{n}{\sigma_{c}}_i=1$ and ${\sigma_{c}}_j\geq 0$ for all $j$
5.  Check the best response condition.

Repeat steps 3,4 and 5 for all potential support pairs.




## 2 by 2 example of support enumeration[](https://notebook.community/drvinceknight/gt/nbs/chapters/05-Support-enumeration#2-by-2-example-of-support-enumeration)

As an example consider the matching pennies game.

$$ A= \begin{pmatrix} 1 & -1\\ -1 & 1 \end{pmatrix}\qquad B= \begin{pmatrix} -1 & 1\\ 1 & -1 \end{pmatrix} $$

1.  Consider $k=1$: so here we are just considering supports of size 1, in other words pairs of pure best responses. The easiest way to identify these is by looking at the best responses:
    
    $$ A= \begin{pmatrix} \underline{1} & -1\\ -1 & \underline{1} \end{pmatrix}\qquad B= \begin{pmatrix} -1 & \underline{1}\\ \underline{1} & -1 \end{pmatrix} $$
    

So there are no pairs.

1.  Thus we start again with $k=2$.
2.  There is only one pair of best responses to be considered: $I=J=\{1, 2\}$.
3.  The equations we need to solve are:
    
    $$-{\sigma_{r}}_1+{\sigma_{r}}_2=v$$ $${\sigma_{r}}_1-{\sigma_{r}}_2=v$$
    
    and
    
    $${\sigma_{c}}_1-{\sigma_{c}}_2=u$$ $$-{\sigma_{c}}_1+{\sigma_{c}}_2=u$$
    
    We don't actually care (or know!) the values of $u, v$ so we in fact solve:
    
    $$-{\sigma_{r}}_1+{\sigma_{r}}_2={\sigma_{r}}_1-{\sigma_{r}}_2$$
    
    $${\sigma_{c}}_1-{\sigma_{c}}_2=-{\sigma_{c}}_1+{\sigma_{c}}_2$$
    
    which gives:
    
    $${\sigma_{r}}_1={\sigma_{r}}_2$$
    
    $${\sigma_{c}}_1={\sigma_{c}}_2$$
    
4.  This gives:
    
    $$\sigma_{r}=(1/2, 1/2)$$
    
    $$\sigma_{c}=(1/2, 1/2)$$
    
5.  Finally we check the best response condition: (we already did this in the previous chapter).
    

Note that for 2 player games with $m=n=2$ step 5 is trivial so in fact to find best mix strategy Nash equilibrium for games of this size simply reduces to finding a solution to 2 linear equations (step 3).

Let us consider a large game:

$$ A= \begin{pmatrix} 1 & 1 & -1\\ 2 & -1 & 0 \end{pmatrix}\qquad B= \begin{pmatrix} 1/2 & -1 & -1/2\\ -1 & 3 & 2 \end{pmatrix} $$

1.  It is immediate to note that there are no pairs of pure best responses.
2.  All possible support pairs are:
    
    -   $I=(1, 2)$ and $J=(1,2)$
    -   $I=(1, 2)$ and $J=(1,3)$
    -   $I=(1, 2)$ and $J=(2,3)$
3.  Let us solve the corresponding linear equations:
    
    -   $I=(1, 2)$ and $J=(1, 2)$:
        
        $$1/2{\sigma_{r}}_1-{\sigma_{r}}_2=-{\sigma_{r}}_1+3{\sigma_{r}}_2$$ $${\sigma_{r}}_1=8/3{\sigma_{r}}_2$$
        
        $${\sigma_{c}}_1+{\sigma_{c}}_2=2{\sigma_{c}}_1-{\sigma_{c}}_2$$ $${\sigma_{c}}_1=2{\sigma_{c}}_2$$
        
    -   $I=(1, 2)$ and $J=(1,3)$:
        
        $$1/2{\sigma_{r}}_1-{\sigma_{r}}_2=-1/2{\sigma_{r}}_1+2{\sigma_{r}}_2$$ $${\sigma_{r}}_1=3{\sigma_{r}}_2$$
        
        $${\sigma_{c}}_1-{\sigma_{c}}_3=2{\sigma_{c}}_1+0{\sigma_{c}}_3$$ $${\sigma_{c}}_1=-{\sigma_{c}}_3$$
        
    -   $I=(1, 2)$ and $J=(2,3)$:
        
        $$-{\sigma_{r}}_1+3{\sigma_{r}}_2=-1/2{\sigma_{r}}_1+2{\sigma_{r}}_2$$ $${\sigma_{r}}_1=2{\sigma_{r}}_2$$
        
        $${\sigma_{c}}_2-{\sigma_{c}}_3=-{\sigma_{c}}_2+0{\sigma_{c}}_3$$ $$2{\sigma_{c}}_2={\sigma_{c}}_3$$
        
4.  We check which supports give valid mixed strategies:
    
    -   $I=(1, 2)$ and $J=(1, 2)$:
        
        $$\sigma_r=(8/11, 3/11)$$ $$\sigma_c=(2/3, 1/3, 0)$$
        
    -   $I=(1, 2)$ and $J=(1, 3)$:
        
        $$\sigma_r=(3/4, 1/4)$$ $$\sigma_c=(k, 0, -k)$$
        
        **which is not a valid mixed strategy.**
        
    -   $I=(1, 2)$ and $J=(2, 3)$:
        
        $$\sigma_r=(2/3, 1/3)$$ $$\sigma_c=(0, 1/3, 2/3)$$
        
5.  Let us verify the best response condition:
    
    -   $I=(1, 2)$ and $J=(1, 2)$:
        
        $$\sigma_c=(2/3, 1/3, 0)$$
        
        $$A\sigma_c^T= \begin{pmatrix} 1\\ 1 \end{pmatrix} $$
        
        Thus $\sigma_r$ is a best response to $\sigma_c$
        
        $$\sigma_r=(8/11, 3/11)$$ $$\sigma_r B=(1/11, 1/11, 2/11)$$
        
        **Thus $\sigma_c$ is not a best response to $\sigma_r$** (because there is a better response outside of the support of $\sigma_c$).
        

-   $I=(1, 2)$ and $J=(2, 3)$:
    
    $$\sigma_c=(0, 1/3, 2/3)$$
    
    $$A\sigma_c^T= \begin{pmatrix} -1/3\\ -1/3 \end{pmatrix} $$
    
    Thus $\sigma_r$ is a best response to $\sigma_c$
    
    $$\sigma_r=(2/3, 1/3)$$ $$\sigma_r B=(0, 1/3, 1/3)$$
    
    Thus $\sigma_c$ is a best response to $\sigma_r$.
    

Thus the (unique) Nash equilibrium for this game is:

$$((2/3, 1/3), (0, 1/3, 2/3))$$





