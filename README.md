# Contribution 1: Incorrect spelling for the Mongolian currency name

**Contribution Number:** 1  

**Student:** Tienyu Zhang 

**Issue:** https://github.com/Doenet/DoenetML/issues/802

**Status:** Phase I Complete

---

## Why I Chose This Issue
DoenetML is an NSF-funded open-source markup language powering interactive math education at scale. This issue is a well-scoped testing task in a TypeScript parser package — directly aligned with my background in software testing (multi-threaded TCP server, AWS CloudWatch component isolation) and my interest in education technology. It lets me make a meaningful contribution to a real academic platform while learning a modern TypeScript/parser testing codebase from the ground up.

---

## Understanding the Issue

### Problem Description
The DAST normalization module (packages/parser/src/dast-normalize/normalize-dast.ts) implements "sugar" — shorthand syntax transformations that convert simplified DoenetML markup into their full canonical DAST (DoenetML Abstract Syntax Tree) form. However, the corresponding test file (packages/parser/test/normalize-dast.test.ts) is missing test cases for three of these sugar transformations: solution/givenAnswer, aside/proof, and pretzel. This means the sugar logic for these components is unverified by automated tests.

### Expected Behavior
For each of the three sugar-enabled component pairs/groups, there should be test cases in normalize-dast.test.ts that verify: (1) the sugar input (shorthand markup) is correctly transformed into the expected full canonical DAST output by the normalizer, and (2) the transformation handles relevant edge cases (e.g. with and without children, with attributes, nested content). Tests should pass in CI on every future PR, protecting these transformations from regressions.

### Current Behavior
No tests exist for the solution/givenAnswer, aside/proof, and pretzel sugar transformations. If a future change accidentally breaks the normalization logic for these components, CI would not catch it — the regression would only surface at runtime in the rendered DoenetML output.

### Affected Components
packages/parser/src/dast-normalize/normalize-dast.ts — contains the sugar transformation logic being tested (read-only reference; no changes needed here)
packages/parser/test/normalize-dast.test.ts — the test file where new test cases for solution/givenAnswer, aside/proof, and pretzel sugar must be added
DoenetML components: <solution>, <givenAnswer>, <aside>, <proof>, and <pretzel> — the markup elements whose normalization sugar is currently untested

---

## Reproduction Process

### Environment Setup

[Notes on setting up your local development environment - challenges you faced, how you solved them]

### Steps to Reproduce

1. [Step 1]
2. [Step 2]
3. [Observed result]

### Reproduction Evidence

- **Commit showing reproduction:** [Link to commit in your fork]
- **Screenshots/logs:** [If applicable]
- **My findings:** [What you discovered during reproduction]

---

## Solution Approach

### Analysis

[Your analysis of the root cause - what's causing the issue?]

### Proposed Solution

[High-level description of your fix approach]

### Implementation Plan

Using UMPIRE framework (adapted):

**Understand:** [Restate the problem]

**Match:** [What similar patterns/solutions exist in the codebase?]

**Plan:** [Step-by-step implementation plan]
1. [Modify file X to do Y]
2. [Add function Z]
3. [Update tests]

**Implement:** [Link to your branch/commits as you work]

**Review:** [Self-review checklist - does it follow the project's contribution guidelines?]

**Evaluate:** [How will you verify it works?]

---

## Testing Strategy

### Unit Tests

- [ ] Test case 1: [Description]
- [ ] Test case 2: [Description]
- [ ] Test case 3: [Description]

### Integration Tests

- [ ] Integration scenario 1
- [ ] Integration scenario 2

### Manual Testing

[What you tested manually and results]

---

## Implementation Notes

### Week [X] Progress

[What you built this week, challenges faced, decisions made]

### Week [Y] Progress

[Continue documenting as you work]

### Code Changes

- **Files modified:** [List]
- **Key commits:** [Links to important commits]
- **Approach decisions:** [Why you chose certain approaches]

---

## Pull Request

**PR Link:** [GitHub PR URL when submitted]

**PR Description:** [Draft or final PR description - much of the content above can be adapted]

**Maintainer Feedback:**
- [Date]: [Summary of feedback received]
- [Date]: [How you addressed it]

**Status:** [Awaiting review / Iterating / Approved / Merged]

---

## Learnings & Reflections

### Technical Skills Gained

[What you learned technically]

### Challenges Overcome

[What was hard and how you solved it]

### What I'd Do Differently Next Time

[Reflection on your process]

---

## Resources Used

- [Link to helpful documentation]
- [Tutorial or Stack Overflow post that helped]
- [GitHub issues or discussions that helped]
