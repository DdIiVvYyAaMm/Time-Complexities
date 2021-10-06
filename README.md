# Time-Complexities
Complexity to generate every combination of every size for a given sequence

Each element in the sequence is part of the combination or not (a binary choice). Since there are n elements, this gives 2n possible combinations.

Using a gray code to iterate over the elements we can make sure that we iterate over every possible combination by only putting in or taking out a single element every time.

Assuming your elements are numbered 1…n we can use the following algorithm. If our current combination Ck contains an even amount of elements, toggle element 1 to get Ck+1. Otherwise, toggle element min(Ck)+1 to get Ck+1.

Starting from the empty combination {} we get:



By separately storing whether we are currently even/odd and flipping it, and storing our combination in sorted order we can always get to the next combination in O(1) time. So it simply takes O(2n) time to generate all combinations.


-------------------------------------------------------------------------------------------------------------

Combinations
Given two integers n and k, return all possible combinations of k numbers out of 1 ... n.

The complexity is O(C(n,k)) which is O(n choose k) . This ends up being equivalent to O(min(n^k, n^(n-k)))
