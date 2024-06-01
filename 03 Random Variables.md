# Random Variables

## Random Variables and Probability

### Sample Spaces

- Discrete / Continuous

### Events (E)

Subset of sample space of random experiment

### Counting Techniques
- Multiplication Rule
  
  $k$ steps, each step $n_i$ choices
  $$\prod_{i=1}^{k} n_i$$
- Permutation Rule
    
    Number of ways $S$ of size $n$ can be arranged

    $$n!$$

  - Subset Permutations
    
    Sequence only $r$ items from set of $n$ items

    $$P_r^n = \frac{n!}{(n-r!)}$$
    
  - Similar Permutations

    Count sequences when not all items are different.

    $$\frac{n!}{n_1!n_2!\dots n_r!}$$

- Combination Rule
  
    Selection or $r$ items from a set, `order doesn't matter`

    $$C_r^n = \frac{n!}{r!(n-r!)}$$

### Probability
- Chance of event
- [0, 1] interval
- $P(E)$ = sum of probabilities of outcomes in $E$

## Discrete Random Variables

### Random Variables `(rv)`
- `rv` denoted by uppercase letter, such as $X$
- Value denoted by lower case letter, such as $x$
- Example: $P(X=x)$

### Probability Distributions
- `rv` $X$ associates the outcomes to a number on the number line.
- **Probability Distribution** of `rv` $X$ is description of probabilities with possible numerical values of $X$
- Probability distribution can be
  1. List of possible values with probabilities
  2. Formula used to calculate the probability (in response to `rv`)

### Probability Mass Function

For a discrete random variable $X$ with possible value $x_1, x_2, \dots, x_n$
`Probability mass function` is a function such that

1. $\displaystyle f(x_i) \geq 0$
2. $\displaystyle \sum_{i=1}^n f(x_i) = 1$
3. $\displaystyle f(x_i) = P(X = x_i)$


### Cumulative Distribution Function

 - Built from `Probability Mass Function` and vice versa

For a discrete random variable $X$, denoted as $F(X)$

1. $\displaystyle F(x) = P(X\leq x) = \sum_{x_i\leq x} f(x_i)$
2. $\displaystyle 0 \leq F(x) \leq 1$
3. If $\displaystyle x \leq y$, then $\displaystyle F(x) \leq F(y)$


### Mean Defined

`mean` or `expected value` of discrete rv $X$ denoted as $\mu$ or $E(X)$

$$\mu = E(X) = \sum_x x\cdot f(x)$$

<u>**Note**</u> $f(x)$ is the probability mass function

`mean` is the **weighted average of the possible values of $X$**, also called **arithmetic mean**

### Variance Defined
`variance` of $X$ denoted as $\displaystyle \sigma ^2$ or $V(X)$ is
$$\sigma^2 = V(X) = E(X-\mu)^2 = \sum_x(x-\mu)^2\cdot f(x) = \sum_x x^2\cdot f(x) - \mu^2$$

[Derivation](./A%20Derivation%20of%20Variance)

`variance` is the **average of the squared deviations** from the distribution mean

### Discrete Uniform Distribution

$$f(x_i) = \frac 1 n$$

Let $X$ be a discrete uniform random variable from $a$ to $b$ for $a < b$
$$
\begin{align}
f(x) &= \frac{1}{b-a+1}\\\\
\mu = E(x) &= \frac 1 2 (a+b)\\\\
\sigma ^2 = V(x) &= \frac {(b-a+1)^2-1}{12}\\\\
\end{align}
$$


### Binomial Random Variables

Characteristics of binomial experiments
1. Fixed number of trials $(n)$
2. Each trial result is `success` or `failure`
3. Probability of success is constant $(p)$
4. Outcomes of successive trials are independent

Probability mass function:
$$f(x) = \binom n x \cdot p^x (1-p)^{n-x}$$

<u>**Note**</u> Out of $n$ trials, there are $x$ success tries $\displaystyle \binom n x$. Probability of getting those success trials is $p^x$. For remaining failed trials $\displaystyle (1-p)^{n-x}$

$$
\begin{align}
\mu = E(x) &= np\\\\
\sigma ^2 = V(x) &= np \cdot (1-p)\\\\
\end{align}
$$

### Poisson Process

Number of events over an interval

Let $\lambda =np = E(x)$ so, $\displaystyle p = \frac \lambda n$

$$
\begin{align}

P(X=x) &= \binom n x \cdot p^x \cdot (1-p)^{n-x}\\\\
&=\binom n x \bigg(\frac \lambda n\bigg)^x \bigg(1-\frac \lambda n\bigg)^{n-x}\\\\
&for: n\rightarrow \infty\\\\

&=\frac{e^{-\lambda }\lambda^x}{x!}\\\\
\end{align}
$$

Probability mass function:
$$f(x) = \frac{e^{-\lambda }\lambda^x}{x!}$$
Mean & Variance
$$
\begin{align}
\mu = E(x) &= \lambda\\\\
\sigma ^2 = V(x) &= \lambda\\\\
\end{align}
$$


## Continuous Random Variables

