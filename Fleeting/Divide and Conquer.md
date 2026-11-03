20261014192925

Tags:

Divide and conquer is a method of solving problems by *recursively* solving smaller *subproblems*.
## + Recursion Trees +
Recursion trees study how the complexity of a divide and conquer scheme is based on three factors
- height of the tree
- time complexity at a level
- number of leaves
### ++ Merge Sort ++
Merge sort is an example of a divide and conquer algorithm. It has the formula $T(n) = 2T(n/2) + cn$, where $cn$ is the time contributed by the root. Every level there are two subproblems with size $n/2$. This means total complexity per level is given by $2 * c \frac{n}{2} = cn$. There are $\log_{2}n$ levels before the leaves are reached, so total complexity is bounded at $\Theta(n\log n)$. 
### ++ Calculating Complexity ++
Given that the goal of a recursion tree is to find the bound of a given tree, the part of the recursion taking up the most time would dictate that. The *balance* of a tree is determined by the complexity of the root and leaves. For example, say an algorithm has complexity $T(n) = 3T(n/4) + cn^{2}$, then every level $l$ has $3^{l}$ subproblems of size $n/4$. The root takes up $cn^{2}$, so the total recursive work per level is $3^{l} \cdot c\left( \frac{n}{4^{l}} \right)^{l} = cn^{2}\left( \frac{3}{16} \right)^{l}$ complexity, meaning this series has worst case $O(n^{2})$ complexity.
### ++ Uneven Recursion ++
Say there's a recursion tree where recurrence is given by $T(n) = T(n/3) + T(2n/3) + cn$. The total nonrecursive work here is still $O(n)$. The subproblem shrinks by $2/3$ with ever level, so the dept given is still $O(\log n)$, giving total complexity of $O(n\log n)$. 
## + The Master Theorem +
The master theorem 
___
# References
