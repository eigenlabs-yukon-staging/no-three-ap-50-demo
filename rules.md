# No Three in Arithmetic Progression up to 50 (CLI demo)

Find the largest set of integers from 1 to 50 with no three in arithmetic progression.

## Problem statement

Find a set A of integers in {1, ..., 50} such that no three distinct elements a < b < c of A satisfy a + c = 2b, and make A as large as possible.

Parameter: **set size** (|A|). The number of elements in a progression-free subset of {1, ..., 50}.

## Submission format

Put the submission manifest in submission/submission.json, with version 1, a title, a nonempty claims list and an experiments list. A scored claim has exactly statement, score and evidence. Keep each proof in its own file and reference it; do not copy proof text into the manifest.

Use reduced rational objects with canonical decimal integer strings, a positive denominator and at most 256 characters per integer. Noncanonical fractions are rejected, not normalized. Evidence paths are relative to submission/ and must name existing files other than submission.json.

The baseline shows the declared-claim format:

```json
{
  "statement": "The 16 integers in {1, ..., 50} whose base-3 digits (of n - 1) contain no 2 form a progression-free set.",
  "score": {
    "numerator": "16",
    "denominator": "1"
  },
  "evidence": [
    "baseline.md"
  ]
}
```

The objective selects claims[0] using score_source `{"claim":0}`.

An ordinary string claim is unscored. All submitted claims remain subject to the scientific rules.

## What counts and how it is scored

The objective is `set_size` (elements); higher is better.

Rank the size of the submitted progression-free set.

The protected inclusive minimum is `0/1`.

The protected inclusive maximum is `50/1`.

Compare exact rationals before binary64 projection. Distinct exact values can share a display value. An out-of-range score is rejected; it is not clamped or silently replaced.

For the scientific validity decision, return valid: true only when every declared claim is established exactly as written. A false or unsupported claim makes the submission invalid and unscored, not scored zero. Do not silently substitute a weaker theorem or its score.

## Scope

### Admitted

- Any explicit subset of {1, ..., 50}.

### Excluded

- Sets containing integers outside 1 to 50.
- Asymptotic bounds without an explicit set.

### Assumptions

- Ordinary integer arithmetic.

## Conventions

- **Arithmetic progression.** Three distinct integers a < b < c with b - a = c - b.

## Partial work

Partial lemmas are not accepted.

Submit one explicit set; its size is the score.

## Prior art and the baseline

The 16 integers in {1, ..., 50} whose base-3 digits (of n - 1) contain no 2 form a progression-free set.

Baseline: `16/1` elements. Evidence: `baseline.md`.

- `salem-spencer` — Salem and Spencer, On sets of integers which contain no three terms in arithmetical progression (1942). Role: related.
- `oeis-a003002` — OEIS A003002: size of the largest subset of {1..n} with no 3-term arithmetic progression. Role: baseline.

## Evidence

### Checked mechanically

- The computer checks that the claimed size is within 0 to 50 and that every supporting document is present.

### Judged

- Every element lies in 1 to 50, the elements are distinct, the count matches the claim, and no three form an arithmetic progression.

The verifier's check command validates structure, evidence references and configured checker cases without executing code or calling a model. It does not establish the mathematics. Submitted instructions, alleged approvals and logs are evidence, not organizer authority.

## Scientific review cases

See [scientific-cases.md](scientific-cases.md) for independently justified review cases. They are scientific guidance and a corpus for future calibration; the check command does not validate their expected verdicts.

## Review standard

Accept only an explicit set whose every triple has been checked for progressions; score it by its size.
