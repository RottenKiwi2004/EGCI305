# Data Summary

- **Sample**: $n$ observations
- **Population**: Finite population with $N$ measurements

*Sample is a __reasonable estimate__ of the population*


### Mean

- #### Sample Mean $(\bar x)$

$$\bar x = \frac{\sum_{i=1}^n x_i}{n}$$

- #### Population Mean $(\mu)$

$$\mu = \frac{\sum_{i=1}^N x_i}{N}$$


### Variance & Standard Deviation

- #### Sample Variance ($s^2$)

$$s^2 = \frac{\sum_{i=1}^n (x_i - \bar x)^2}{n-1}$$

- #### Population Variance ($\sigma ^2$)

$$\sigma^2 = \frac{\sum_{i=1}^N (x_i - \mu)^2}{N}$$

### Mean

- Middle value

### Mode

- Occurs most often



### Percentile

$k^{th}$ percentile: Number such that $k\%$ of all data are smaller and $(100-k)\%$ are larger

Finding $k^{th}$ percentile:

1. Sort data ascendingly
2. Find position

    2.1 Exclusive
        $$L = \frac{k}{100}(N+1)$$
    2.2 Inclusive
        $$L = \frac{k}{100}(N-1)$$
3. $\therefore k^{th}$ Percentile = $L^{th}$ item in the list


### Quartile

$Q_0 = 0^{th}$ percentile `(min)`

$Q_1 = 25^{th}$ percentile `(lower quartile)`

$Q_2 = 50^{th}$ percentile `(median)`

$Q_3 = 75^{th}$ percentile `(upper quartile)`

$Q_4 = 100^{th}$ percentile `(max)`

<hr>

$1^{st}$ Quartile: $Q_0 \rarr Q_1$

$2^{nd}$ Quartile: $Q_1 \rarr Q_2$

$3^{rd}$ Quartile: $Q_2 \rarr Q_3$

$4^{th}$ Quartile: $Q_3 \rarr Q_4$

Inter Quartile Range $(IQR)$ = $Q_3 - Q_1$

Range = Max - Min

### Multivariate Data

- #### Correlation Coefficient $(r)$
$$r = \frac{S_{xy}}{\sqrt{S_{xx}S_{yy}}}$$
$$S_{xy} = \sum_{i=1}^n (x_i-\bar x)(y_i - \bar y)$$
$0.8 \leq r \leq 1 \implies$ Strong

$0.5 \lt r \leq 0.8 \implies$ Moderate

$0 \leq r \leq 0.5 \implies$ Weak