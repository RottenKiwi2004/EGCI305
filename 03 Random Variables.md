# <u>Random Variables</u>

## <u>Random Variables and Probability</u>

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

<div style="page-break-after: always;"></div>

## <u>Discrete Random Variables</u>

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
<div style="page-break-after: always;"></div>

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

<div style="page-break-after: always;"></div>

Probability mass function:
$$f(x) = \frac{e^{-\lambda }\lambda^x}{x!}$$
Mean & Variance
$$
\begin{align}
\mu = E(x) &= \lambda\\\\
\sigma ^2 = V(x) &= \lambda\\\\
\end{align}
$$


## <u>Continuous Random Variables</u>

Number of possible value $X$ is uncountably infinite

### Probability Density Function

- Describes the probability distribution of a continuous random variable

For continuous random variable $X$, Probability Density Function, $f(x)$ is a function such that

1. $\displaystyle f(x) \geq 0$ ; function is always non-negative
2. $\displaystyle \int_{-\infty}^{\infty}f(x)\, \mathrm dx =1$ 
3. $\displaystyle P(a \leq X \leq b) = \int_{a}^{b}f(x)\, \mathrm dx$ 
4. $\displaystyle f(x) = 0$ ; no area at exactly at $x$

### Histograms

- A continuous porbability distribution $f(x)$ is an approximation of a histogram.
- A bar of histogram has the same area of integral of those limits

### Area of a point
If $X$ is a continuous random variable, 

$$P(x_1 \leq X \leq x_2) = P(x_1 \lt X \leq x_2) = P(x_1 \leq X \lt x_2) = P(x_1 \lt X \lt x_2) = $$

This implies that $P(X=x) = 0$


### Cumulative Distribution Functions

$$F(x) = P(X\leq x) = \int_{-\infty}^x f(u)\, \mathrm du \text{ for } -\infty <x< \infty$$

<u>**Note**</u> 
- **Probability Density Function** is the derivative of the **Cumulative Distribution Function**
- **Cumulative Distribution Function** is the derivative of the **Probability Density Function**

### Mean and Variance

$$
\begin{align}
\mu &= E(X) &= \int_{-\infty}^\infty x\cdot f(x)\, \mathrm dx &\\\\
\sigma^2 &= V(X) &= \int_{-\infty}^\infty (x-\mu)^2\cdot f(x)\, \mathrm dx &= \int_{-\infty}^\infty x^2\cdot f(x)\, \mathrm dx - \mu^2\\\\
\end{align}
$$

<div style="page-break-after: always;"></div>

### Continuous Uniform Distribution

$$
\begin{align}
f(x) &= \frac 1 {b-a} \text{ for } a \leq x \leq b\\\\
\mu = E(X) &= \frac {a+b} 2\\\\
\sigma^2 = V(X) &= \frac{(b-a)^2} {12}
\end{align}
$$

<div style="display:flex;justify-content:center;align-content:center;width:100%;">
<img src="/Assets/continuousUniformDistribution.png" height="140px">
</div>

##### Continuous Uniform Cumulative Distribution Function
$$
\begin{align}
F(x) &= 0\,\,\,&;&\,\,\, x < a\\\\

F(x) &= \frac{x-a}{b-a}\,\,\,&;&\,\,\, a \leq x \leq b\\\\

F(x) &= 1\,\,\,&;&\,\,\, x > b\\\\
\end{align}
$$
<div style="display:flex;justify-content:center;align-content:center;width:100%;">
<img src="/Assets/continuousUniformCDF.png" height="140px">
</div>

### Normal Distribution

- Also known as Gaussian distribution
- Location and spread determined by mean and standard deviation

$$
f(x) = \frac 1 {\sigma\sqrt{2\pi}} e^{\frac{-(x-\mu)^2}{2\sigma^2}}
$$

<div style="display:flex;justify-content:center;align-content:center;width:100%;">
<img src="/Assets/normalDistribution.png" height="140px">
</div>

##### Standard Normal Distribution
$$\mu = 0, \sigma^2 = 1$$
$$\Phi(z) = P(Z\leq z) = F(z) = \int_{-\infty}^{\infty}\frac 1 {\sqrt{2\pi}} e^{\frac{-x^2}{2}} \mathrm ds$$

<div style="page-break-after: always;"></div>

##### Standardising

Suppose $X$ is normal random variable with $\mu$ and $\sigma^2$
$$
P(X \leq x) = P\bigg(\frac{X-\mu}\sigma \leq \frac{x-\mu}\sigma\bigg) = P(Z \leq z)
$$

$Z$ is standard normal random variable

$\displaystyle z = \frac {x-\mu}\sigma$, obtained by standardising $X$

<div style="display:flex;justify-content:center;align-content:center;width:100%;">
<img src="/Assets/standardNormalDistribution.png" height="140px">
</div>


## <u>Normal Approximation to Binomial and Poisson Distributions</u>

- As their means increase, Binomial and Poisson distributions become more bell-shaped and symmetric
- Normal distribution is a good approximation
	- For Binomial distribution if $np > 5$ and $n(1-p) > 5$
	- For Poisson distribution if $\lambda > 5$

### Normal Approximation to Binomial
If $X$ is binomial random variable with parameters $n$ and $p$

$$
Z = \frac{X - np}{\sqrt{np(1-p)}}
$$

To approximate a binomial probability with normal distribution

$$
P(X\leq x) = P(X \leq x + 0.5) = P\bigg(Z \leq \frac
{x + 0.5 - np}
{\sqrt{np (1-p)}}
\bigg)
$$
$$
P(X\lt x) = P(X \leq x - 0.5) = P\bigg(Z \leq \frac
{x - 0.5 - np}
{\sqrt{np (1-p)}}
\bigg)
$$

$$
\begin{align}
\therefore P(X>x) = P(X\geq x) = P(X > x + 0.5)\\\\
\therefore P(X=x) = P(x-0.5 \lt X \lt x + 0.5)\\\\
\end{align}
$$


### Normal Approximation to Poisson

If $X$ is binomial random variable with parameters $E(X) = \lambda$ and $V(X) = \lambda$

$$
Z = \frac{X - \lambda}{\sqrt{\lambda}}
$$

<div style="page-break-after: always;"></div>

## <u>More than One Random Variable and Independence</u>

- Some random variables are not independent.

- A joint probability distribution describes the behaviour of several random variables
- The graph of the distribution is 3D: $(x, y, f(x,y))$


### Joint Probability Mass Function

1. $\displaystyle f_{XY}(x, y) \geq 0$
2. $\displaystyle \sum_x\sum_yf_{XY}(x, y) = 1$
3. $\displaystyle f_{XY}(x, y) = P(X=x, Y=y)$

### Joint Probability Density Function

1. $\displaystyle f_{XY}(x, y) \geq 0 \text{ for all } x,y$
2. $\displaystyle \int_{-\infty}^{\infty}\int_{-\infty}^{\infty}f_{XY}(x, y)\, \mathrm dx \mathrm dy = 1$
3. $\displaystyle P\big((X, Y) \subset R) = \iint\limits_R f_{XY}(x,y)\, \mathrm dx \mathrm dy$

### Marginal Probability Distribution

- Discrete
	- $\displaystyle f_X(x) = \sum_y f(xy)$
	- $\displaystyle f_Y(y) = \sum_x f(xy)$
- Continuous
	- $\displaystyle f_X(x) = \int\limits_y f_{XY}(xy)\,\mathrm dy$
	- $\displaystyle f_Y(y) = \int\limits_x f_{XY}(xy)\,\mathrm dx$

### Mean and Variance of Marginal Distribution

- Discrete
	- $\displaystyle E(X) = \sum_R x\cdot f_X(x) = \mu_X$
	- $\displaystyle E(Y) = \sum_R y\cdot f_Y(y) = \mu_Y$
	- $\displaystyle V(X) = \sum_R x^2\cdot f_X(x) - \mu_X^2$
	- $\displaystyle V(Y) = \sum_R y^2\cdot f_Y(y) - \mu_Y^2$
- Continuous
	- $\displaystyle E(X) = \int\limits_R x\cdot f_X(x) \,\mathrm dx = \mu_X$
	- $\displaystyle E(Y) = \int\limits_R y\cdot f_Y(y) \,\mathrm dy = \mu_Y$
	- $\displaystyle V(X) = \int\limits_R x^2\cdot f_X(x) \,\mathrm dx - \mu_X^2$
	- $\displaystyle V(Y) = \int\limits_R y^2\cdot f_Y(y) \,\mathrm dy - \mu_Y^2$

<div style="page-break-after: always;"></div>

### Conditional Probability Distribution

$$P(B | A) = \frac {P(A\cap B)}{P(A)}$$

### Conditional Probability Density Function
The conditional probability density function $Y$ given $X=x$
$$f_{Y|x}(y) = \frac{f_{XY}(x, y)}{f_X(x)} \text{ for } f_X(x) > 0$$

Which satisfies the following properties
1. $\displaystyle f_{Y|x}(y) \geq 0$
2. $\displaystyle \int f_{Y|x}(y)\, \mathrm dy = 1$
3. $\displaystyle P(Y \subset B \,| \,X = x) = \int\limits_B f_{Y|x}(y)\, \mathrm dy$


### Joint Random Variable Independence

Knowledge of the values of $X$ does not change any of the probabilities associated with the values of $Y$


### Properties of Independence

If one of the following properties is true, the others will also be true and $X, Y$ are **independent**

1. $\displaystyle f_{XY}(x, y) = f_X(x) \cdot f_Y(y)$
2. $\displaystyle f_{Y|x}(y) = f_Y(y)$ ; for all $x$ and $y$ with $f_X(x) > 0$
3. $\displaystyle f_{X|y}(x) = f_X(x)$; for all $x$ and $y$ with $f_Y(y) > 0$
4. $\displaystyle P(X \subset A, Y \subset B) = P(X \subset A) \cdot P(Y \subset B)$

## <u>Functions of Random Variables</u>

- A function of random variables is also a random variable
- Given random variables $X_1, X_2, \dots, X_p$ and constants $c_1, c_2, \dots, c_p$

$$Y = c_1X_1 + c_2X_2+ \dots+ c_pX_p$$

- $Y$ is a linear combination of $X_1, X_2, \dots, X_p$

$$
\begin{align}
E(Y) &= c_1E(X_1) + c_2E(X_2)+ \dots+ c_pE(X_p)\\\\
V(Y) &= c_1^2V(X_1) + c_2^2V(X_2)+ \dots+ c_p^2V(X_p) + 2\sum_{i<j}\sum c_ic_j \mathrm{cov}(X_iX_j)
\end{align}
$$

If $X_1, X_2, \dots, X_p$ are independent, $\mathrm{cov}(X_iX_j) = 0$
$$V(Y) = c_1^2V(X_1) + c_2^2V(X_2)+ \dots+ c_p^2V(X_p)$$

<u>**Note**</u> $\mathrm{cov}(X,Y)$ or $\sigma_{XY}$ is the covariance between the random  variables $X$ and $Y$

### Mean and Variance on Average

If $\displaystyle \bar X = \frac{X_1+ X_2+ \dots+ X_p}{p}$ and $E(X_i) = \mu$, then $\displaystyle E(\bar X) = \frac{p\cdot\mu}p = \mu$

If $X_i$ are independent with $\displaystyle V(X_i) = \sigma^2$, then $\displaystyle V(\bar X) = \frac{p\cdot\sigma^2}{p^2} = \frac {\sigma^2}{p}$
