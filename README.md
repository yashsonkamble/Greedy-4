# Greedy-4

## Problem1: Minimum Path Form String formation

From a given string, we can form a subsequence of that string by removing some characters (only if required).

Given two strings source and target, return the minimum number of subsequences of source such that their concatenation equals target. If impossible, return -1.

Example 1:

Input: source = "abc", target = "abcbc"

Output: 2

Explanation: The target "abcbc" can be formed by "abc" and "bc", which are subsequences of source "abc".

Example 2:

Input: source = "abc", target = "acdbc"

Output: -1

Explanation: The target string cannot be constructed from the subsequences of source string due to the character "d" in target string.

Example 3:

Input: source = "xyz", target = "xzyxz"

Output: 3

Explanation: The target string can be constructed as follows "xz" + "y" + "xz".

Notes:

Both the source and target strings consist of only lowercase English letters from "a"-"z".

The lengths of source and target string are between 1 and 1000.

## Problem2:  Equal Row From Minimum Domino Rotations 

Given a row of dominoes, A[i] and B[i] represent the top and bottom halves of the i-th domino.

We may rotate the i-th domino, so that A[i] and B[i] swap values.

Find the minimum number of rotations so that all the values in A are the same, or all the values in B are the same.

If it cannot be done, return -1.

Example 1:

Input: A = [2,1,2,4,2,2], B = [5,2,6,2,3,2]

Output: 2

Explanation: 

The first figure represents the dominoes as given by A and B: before we do any rotations.

If we rotate the second and fourth dominoes, we can make every value in the top row equal to 2, as indicated by the second figure.

Example 2:

Input: A = [3,5,1,2,3], B = [3,6,3,3,4]

Output: -1

Explanation: 

In this case, it is not possible to rotate the dominoes to make one row of values equal.

Note:

1 <= A[i], B[i] <= 6

2 <= A.length == B.length <= 20000

## Problem3: Bikes in a Campus

Given a 2D grid representation of a campus having N workers and M bikes, with N <= M. Each worker and bike is a 2D coordinate on this grid.

Our goal is to assign a bike to each workerin such a way that we choose the (worker, bike) pair with the shortest Manhattan distance between each other, and assign the bike to that worker. (If there are multiple (worker, bike) pairs with the same shortest Manhattan distance, we choose the pair with the smallest worker index; if there are multiple ways to do that, we choose the pair with the smallest bike index). We repeat this process until there are no available workers.

The Manhattan distance between two points p1 and p2 is Manhattan(p1, p2) = |p1.x - p2.x| + |p1.y - p2.y|.

Return a vector ans of length N, where ans[i] is the index (0-indexed) of the bike that the i-th worker is assigned to.

Example 1:



Input: workers = [[0,0],[2,1]], bikes = [[1,2],[3,3]]

Output: [1,0]

Explanation: 

Worker 1 grabs Bike 0 as they are closest (without ties), and Worker 0 is assigned Bike 1. So the output is [1, 0].

Example 2:



Input: workers = [[0,0],[1,1],[2,0]], bikes = [[1,0],[2,2],[2,1]]

Output: [0,2,1]

Explanation: 

Worker 0 grabs Bike 0 at first. Worker 1 and Worker 2 share the same distance to Bike 2, thus Worker 1 is assigned to Bike 2, and Worker 2 will take Bike 1. So the output is [0,2,1].
Note:

0 <= workers[i][j], bikes[i][j] < 1000

All worker and bike locations are distinct.

1 <= workers.length <= bikes.length <= 1000
