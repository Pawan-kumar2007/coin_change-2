
# Coin Change II

## Approach

Used recursion with two choices:

* **Include:** Use the current coin and keep the same index.
* **Exclude:** Skip the current coin and move to the next index.

## Base Cases

* `amount == 0` → return `1`
* `index >= coins.length` → return `0`
* `amount <= 0` → return `0`

## TLE Reason

After submission, the solution showed **TLE** because the recursive approach calculates the same `(amount, index)` states multiple times.

**Improvement:** Use **Memoization / Dynamic Programming** to avoid repeated calculations.

## Complexity

* Time: Exponential in worst case
* Space: `O(amount + coins.length)` recursion stack
