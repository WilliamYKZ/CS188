# HomeWork 0

## Question 1 Probabilistic Inference

Your box of cereal may be a contest winner! It's rattling, which 100% of winning boxes do. Of course 1% of all boxes rattle and only one box in a million is a winner. What is the probability that your box is a winner?

### Answer

Recall Bayes's rule, which states that $P(A|B)=\frac{P(B|A) \cdot P(A)}{P(B)}$

The question asks to find $P(winner|rattling)$ given that $P(rattling)=.01$, $P(winner)=.000001$ and $P(rattling|winner)=1$

and using Bayes' rule we can get $.0001$

### Question 

What is different between $,$ and $|$ in the stat.



## Question 2 Events

You are playing a solitaire game in which you are dealt three cards without   replacement from a simplified deck of 10 cards (marked 1 through 10). You win if   one of your cards is a 10 or if all of your cards are odd.

How many winning hands are there if different orders are different hands?

### Answer

Because 10 is an even number, the two events that cause a winning hand are nutually exclusive, meaning there is no hand which both contains a 10 and three odd cards. The set of winning hands is the union of the sets satisfying either condition, and because they are nutually exclusive, the probability of each of the sets can be determined separately and then added together. 

- Case 1: if one card is 10

  First, condifer the case in which the first card in the hand is a 10. There are 9 remaining cards for the second spot, and 8 possibilities for the thrid. Thus, the total number of hands in which the first card is a 10 is $9 \cdot 8=72$. This is same if you set either the second or third spots to 10 as well. Since these three events are mutually disjoint, the sets can be combined, so there are $72\cdot 3=216$ possible hands containing a 10

- Case 2: if all cards are odd

  There are 5 odd cards in the deck: 1,3,5,7,9. The first card can be any of the 5 possibilities, then the second can be any of the remaining 4, and the last any of the final 3. This gives $5\cdot 4\cdot 3=60$.

We add together and get **276**



What is your chance of winning?

### Answer

The change of winning is equal to $\frac{number \ of \ winning\ hands}{total\ number \ of \ hand}$. The number of total hands is found in the same way as the number of odd hands: $10\cdot 9\cdot 8= 720$ different hands. Plugging in the number of winning hands found in the first question will get **.383**





## Question 3 Expectations

Someone rolls a fair six-sided die and you win points equal to the number shown. 

What is the expected number of point after one roll?

### Answer

The die is fair, so each side comes up with an equal probability, which, since there are 6 sides, is $\frac{1}{6}$. The expectation of a random variable $X$ is equal to $\sum_{x \in \operatorname{domain}(X)} x * P(x)$, Where domain($X$) denotes the set of all values $X$ could take on. In the case of this probelem, the random variable is the outcome of rolling a die, hence the domain is $\{1,2,3,4,5,6\}$, and each value has equal probability of $\frac{1}{6}$. Thus, the expectation is $\frac{1}{6} \sum_{x=1}^{6} x=\frac{1}{6} * 21=3.5$



What is the expected number of point after two roll?

### Answer

The part could be done in the same way as part 1, however, as the number of possible values and probabilities grows, it becomes very tedious to enumerate all the outcomes. We will use the linearity of expectation, meaning $\mathrm{E}\left[X_{1}+X_{2}\right]=\mathrm{E}\left[X_{1}\right]+\mathrm{E}\left[X_{2}\right]$. Concretely, let $X_1$ and $X_2$ correspond to the outcome for die 1 and die 2 respectively. Then we are asked to compute: $\mathrm{E}\left[X_{1}+X_{2}\right]=\mathrm{E}\left[X_{1}\right]+\mathrm{E}\left[X_{2}\right]$. Since the value of rolling a die is independent of the value that has come up on previous rolls, these expectations are identical. $\mathrm{E}\left[X_{1}\right]=\mathrm{E}\left[X_{2}\right]=3.5$. Thus the answer is 7.



What is the expected number of point after 100 roll?

### Answer

$\sum_{i=1}^{100} \mathrm{E}\left[X_{i}\right]=100 * 3.5=350$



## Question 4 Conditional Probabilities

Select all of the following statements that are true for all joint distributions over $X$ and $Y$.

![](https://github.com/WilliamYKZ/Picture/raw/main/Picture/Screen%20Shot%202022-07-27%20at%205.15.04%20AM.png)

### Answer

a) is only true in general if x and y are independent. 

b) $P(x \mid y)=\frac{P(x, y)}{P(y)} \rightarrow \frac{P(x, y) * P(y)}{P(y)}=P(x, y)$

c) This is only true in general if x and y are independent: $P(x \mid y) P(y \mid x)=\frac{P(x, y) P(x, y)}{P(x) P(y)}$

d) This is only true in general if x and y are independent. 



## Question 5 Logarithms

Select all of the following statements that are true. 

![](https://github.com/WilliamYKZ/Picture/raw/main/Picture/Screen%20Shot%202022-07-27%20at%206.21.07%20AM.png)

a) This is not true $2^{x*y}=(2^x)^y$



