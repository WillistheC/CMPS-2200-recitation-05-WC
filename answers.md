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

Work: construct_output, as I have written it, loops through positions once, and it performs one command per line. Then it performs one final command

This gives $W(n) = O(n)$ as it iteratively adds one item to the array for every $n$ item in a

Span: construct_output, as I have written it, sequentially adds one item for every $n$ item in a, so the longest chain of dependency is the whole algorithim

This gives an identical $S(n) = O(n)$

- **6) (2 pts)** What is the work and span of `supersort`?

Work: supersort calls 3 commands that do linear work, so $W(n) = O(3n) = O(n)$

Span: supersort calls 2 commands of linear span and one of logarithmic span, so $S(n) = O(2n + logn) = O(n)$

- **8) (2 pts)** What is work and span of `count_values_mr`?

Work: The map-reduce version still does the same linear work; optimizing the span does not change it

So, $W(n) = O(n)$

Span: This version allows each list to be split into pieces, and the longest chain of dependency is the longest branch

If it is split into $k$ pieces, the height of the longest branch is $h = log{k}{n}$

So, the span is logorithmic; $S(n) = O(logn)$
