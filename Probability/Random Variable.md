# Probability

## Random Variable

### Distribution function / Cumulative distribution function
$$
F_X(x) = P(X\leq x)\space x\in \R 
$$

**Properties**
1. F_X(-\infty)=0 and F_X(+\infty)=1
2. whenever a\leq b, then F_X(a)\leq F_X(b), i.e F_Xis non-decresing on \R
3. for all x\in \R, \lim_{h\to0^+}F_X(x+h)=F_X(x), i.e F_Xis continuous on the right

### Probability mass function

Abbv.: p.m.f
$$
p_X(x)=P(X=x)\space x\in \R
$$
**Properties**

1. 0\leq p_X(x)\leq1
2. \sum_{x\in \R_X}p_X(x)=1

The probability density function

Abbv: p.d.f

**Definition:**
$$
f_X(x) = \frac{dF_X(x)}{dx}\space x\in \R
$$


## Moment

### Expected value

**Definition**
$$
E(X)=\sum_{x\in \R_X}xp_X(x)
$$


**Definition**

The kth moment of the random variable X around a value c is $E[(X-c)^k]$

### Percentile

## Distributions

### Uniform distribution

**Definition**

The Uniform distribution on the interval [a, b], written $X\sim U(a,b)$

### Distribution function
$$
F_X(x)=\left\{\begin{array}{**lr**} 0, & x\leq a \\
            	\frac{x-a}{b-a}, & a<x\le b \\  
             1, &   b<x\end{array} \right.
$$


Probability density function

f_X(x)=\left\{\begin{array}{**lr**} 0, & x\leq a \\  
            	\frac{1}{b-a}, & a<x\le b \\  
             0, &   b<x\end{array} \right.



Properties

E(X)=\frac{a+b}{2}


