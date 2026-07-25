
# Observation

For
<img width="417" height="40" alt="image" src="https://github.com/user-attachments/assets/11bd867a-31c8-4087-bcbe-095356618fbe" />


## Proof Idea

- If `b | a` and `b | c`:
  - `lcm(a, b) = a`
  - `lcm(b, c) = c`
  - Hence,
 <img width="417" height="40" alt="image" src="https://github.com/user-attachments/assets/0d9cd434-2bd1-4719-9fea-04a6076f5874" />

- Otherwise, assume `b ∤ a`.
  - Both LCMs are divisible by `b`, so their GCD is also divisible by `b`.
  - Thus, `gcd(a, c)` is divisible by `b`.
  - Since `gcd(a, c) | a`, we get `b | a`, a contradiction.

**Therefore, the only valid triples satisfy `b | a` and `b | c`.**

## Counting

For a fixed `b`:

- Number of multiples of `b` in `[1, n]`:

 integer value of (n/b)

- `a` and `c` are chosen independently.

So, the number of valid triples is

square of integer value of (n/b)

Hence,

sum of all these values from b=1 to n;
**Time Complexity:** `O(n)`
