# No Three in Arithmetic Progression up to 50 (CLI demo): scientific review cases

These expected verdicts follow from the arguments below, independently of model verdicts. This is a public review corpus, not live reviewer qualification or an executable checker test suite.

## base-3-baseline

Expected verdict: `accept_scored`.

### Claim or argument

The 16-element base-3 set is progression-free.

### Assessment

Two numbers with digits 0 and 1 average to a number with digits 0 and 1 only when they agree digit by digit.

## contains-progression

Expected verdict: `reject`.

### Claim or argument

The set {1, 2, 3, 10} has no three-term progression.

### Assessment

1, 2, 3 is a progression with common difference 1.
