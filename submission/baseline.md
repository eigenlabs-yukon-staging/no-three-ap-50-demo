# Baseline: 16 elements

A = {1, 2, 4, 5, 10, 11, 13, 14, 28, 29, 31, 32, 37, 38, 40, 41}

Each element is n where n - 1 has only the digits 0 and 1 in base 3.
If a + c = 2b for a, b, c in A, then (a-1) + (c-1) = 2(b-1). Adding two
numbers with digits 0 and 1 has no carries, and 2(b-1) has digits 0 and 2,
so a-1 and c-1 agree at every digit, giving a = c. So A has no three-term
arithmetic progression, and |A| = 16.
