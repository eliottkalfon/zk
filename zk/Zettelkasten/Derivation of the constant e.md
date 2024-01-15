
202401100929
Status: #idea
Tags: #mathematics 

# Derivation of the constant e

By definition, the constant $e$ is defined by $(1 + \frac{1}{n})^n$.

The reason why is still to be investigated.

This can be expanded using the [[Binomial theorem]], as $(1 + \frac{1}{n})^n$ is of the form $(a+b)^k$, with $a = 1, $b = \frac{1}{n}$ and $n = k$.

From the Binomial Theorem, we get:

$$ (a + b)^n = \sum_{k=0}^{n} \left[ \frac{n!}{k!(n-k)!} a^{n-k} b^k \right] $$
Then:

$(1 + \frac{1}{n})^n = \frac{n!}{0! \cdot n!} \cdot \frac{1}{n}^0 + \frac{n!}{1! \cdot (n-1)!} \cdot \frac{1}{n}^1 +  \frac{n!}{2! \cdot (n-2)!} \cdot \frac{1}{n}^2 + ... + \frac{n!}{n! \cdot 0!} \cdot \frac{1}{n}^n$
$(1 + \frac{1}{n})^n =  1 + \frac{n}{n} + \frac{n(n-1)}{2! \cdot n^2} + \frac{n(n-1)(n-2)}{3! \cdot n^3} +... + \frac{1}{n^n}$

When $n$ tends towards infinity, $n(n-1)(n-2)$ gets very close to $n^3$, following this reasoning:
$e = \lim_{n \to \infty} (1 + \frac{1}{n})^n = 1 + 1 + \frac{1}{2!} + \frac{1}{3!} + ... + \frac{1}{n!} + ...$










___
# References

[[Calculus Made Easy]] - Silvanus Thompson, ISBN: 1629920282, [ebook](https://calculusmadeeasy.org/)