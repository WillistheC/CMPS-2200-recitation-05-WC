# CMPS 2200 Recitation 05
## Answers

**Name:**_________________________
**Name:**_________________________


Place all written answers from `recitation-05.md` here for easier grading.




- **3) (2 pts)** What is the work and span of `get_positions`? (assume our more efficient version of `scan` from class)

Work: The span-efficient version looks like $W(n) = 2W(\frac{n}{2}) + 1$

This gives level $i$ has $2^{i}$ sub-problems of size $\frac{n}{2^{i}}$

This gives a total of $2n - 1$ problems, each with a work cost of 1

So, $W(n) = O(2n-1) = O(n)$

Span: The span-efficient version looks like $S(n) = S(\frac{n}{2}) + 1

All branches are of equal length, and the longest chain of dependency is the max length of the branch

The branch ends when $2^{h} = n$, so $h = log{_2}{n}$

Therefore, $S(n) = O(logn)$

- **5) (2 pts)** What is the work and span of `construct_output`?

Work:


- **6) (2 pts)** What is the work and span of `supersort`?




- **8) (2 pts)** What is work and span of `count_values_mr`?
