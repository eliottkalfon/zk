
202401100932
Status: #idea
Tags: #mathematics 

# Binomial theorem

The binomial theorem is a way to expand the sum of two numbers raised to an integer power $n$

$$ (a + b)^n = \sum_{k=0}^{n} \left[ \frac{n!}{k!(n-k)!} a^{n-k} b^k \right] $$

This fraction $\frac{n!}{k!(n-k)!}$ can be difficult to understand, its purpose is to choose $k$ elements out of $n$, without considering the order of the items. It is also noted $\binom{n}{k}$. See [[Permutations and combinations]] for more details.

Thinking of a simple example, let $n = 3$ and $k = 2$. In the binomial context, this could be interpreted as three trials and two successes.

Following the fraction above, we get:

$\binom{3}{2} = \frac{3!}{2! \cdot 1!} = 3$

Which implies that with 3 trials, there are three different ways to have 2 successes.

It has many applications, and can be used in the [[Derivation of the constant e]].

## Numerical example

$(a+b)^3 = \frac{3!}{0! \cdot 3!}a^3b^0 + \frac{3!}{1! \cdot 2!}a^2b^1 + \frac{3!}{2! \cdot 1!}a^1b^2 + \frac{3!}{3! \cdot 0!}a^0b^3$ 

Which simplifies to: $a^3 + 3a^2b^1 + 3a^1b^2 + b^3$

Verifying with $a=2$ and $b = 1$
$(2 + 1)^3 = 27$ and $2^3 + 3 \cdot 2^2 \cdot 1 + 3 \cdot 2 \cdot 1 + 1 = 27$


___
# References
[[Calculus Made Easy]] - Silvanus Thompson, ISBN: 1629920282, [ebook](https://calculusmadeeasy.org/)
