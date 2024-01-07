
202401031842
Status: #idea
Tags: #mathematics [[Calculus Made Easy]]

# Differentiating with the dx notation

$dx$ represents a very small amount of $x$. Differentiating an expression $y$ with regards to a variable $x$ aims at determining the impact of a very small variation of $x$ (noted $dx$) on the value of $y$. This is also noted $\frac{dy}{dx}$.

Thinking about it in this way allows us to differentiate functions using the rules of algebra.

For example, to differentiate $f(x) = 2x$ or $y = 2x$

We get: 

$$
\begin{align} 
y + dy &= 2(x + dx) \\
dy &= 2x + 2dx - y \\
dy &= 2x + 2dx - 2x \\
\frac{dy}{dx} &= 2
\end{align} 
$$

We can use the same approach to differentiate the product of two expressions $u$ and $v$ (both functions of variable $x$), defining $y = u * v$ .

Using the similar approach:
$$
\begin{align} 
y + dy &= (u + du)(v + dv) \\
y + dy &= uv + u \cdot dv + v \cdot du + du \cdot dv \\
dy &= uv + u \cdot dv + v \cdot du + du \cdot dv - uv \\
dy &= u \cdot dv + v \cdot du && \text{$du \cdot dv$ is too small of a quantity} \\
\frac{dy}{dx} &= u \cdot \frac{dv}{dx} + v \cdot \frac{du}{dx} && \text{dividing both sides by $dx$}
\end{align} 
$$

Another example, differentiating $y = \sqrt{x}$:
$$
\begin{align} 
y + dy &= \sqrt{x + dx} \\
(y + dy)^2 &= x + dx \\
y^2 + 2y \cdot dy + (dy)^2 &= x + dx \\
2y \cdot dy + (dy)^2 &= dx && \text{subtracting $y^2$ from both sides} \\
2y \cdot dy &= dx && \text{ignoring $(dy)^2$ because it is a second-order small quantity} \\
dy &= \frac{dx}{2y} && \text{dividing both sides by $2y$} \\
\frac{dy}{dx} &= \frac{1}{2y} && \text{dividing both sides by $dx$}
\end{align}
$$


___
# References
*Calculus Made Easy* - Silvanus Thompson, ISBN: 1629920282, [ebook](https://calculusmadeeasy.org/)
