---
description: Diving Deep into Bitcoin
---

# Coding Bitcoin

Finite Fields

```
def __init__(self, num, prime):
if num >= prime or num < 0: 1
              error = 'Num {} not in field range 0 to {}'.format(
                  num, prime - 1)
raise ValueError(error) self.num = num 2 self.prime = prime
      def __repr__(self):
          return 'FieldElement_{}({})'.format(self.prime, self.num)
      def __eq__(self, other):
          if other is None:
return False
return self.num == other.num and self.prime == other.prime
```

> Fermat’s Little Theorem

> ```text
> The resulting numbers might not be in the right order, but the same numbers are in both sets.
> We can then multiply every element in both sets to get this equality:
> 1⋅2⋅3⋅...⋅(p-2)⋅(p-1) % p = n⋅2n⋅3n⋅...⋅(p-2)n⋅(p-1)n % p
> The left side is the same as (p-1)! % p where ! is the factorial (e.g. 5! = 5⋅4⋅3⋅2⋅1). The right side, we can gather up all the `n’s and get:
> (p-1)!⋅n(p-1) % p
> Thus:
> (p-1)! % p = (p-1)! ⋅n(p-1) % p
> The (p-1)! on both sides cancel giving us: 1 = n(p-1) % p
> This proves Fermat’s Little Theorem
> ```



