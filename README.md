# Contribution 1: Incorrect spelling for the Mongolian currency name

**Contribution Number:** 1  

**Student:** Tienyu Zhang 

**Issue:** https://github.com/medusajs/medusa/issues/14071

**Status:** Phase I Complete

---

## Why I Chose This Issue

A simple typo/data fix in the currency list — the name for the Mongolian currency (Tögrög) is misspelled. No deep codebase knowledge needed. Perfect first PR.

Self-contained, clearly scoped, no environment setup required to understand the fix. Only need to find the currency data file, fix a misspelled name, done. It'll teach me the PR workflow without any code risk.

---

## Understanding the Issue

### Problem Description

The Mongolian currency's spelling is incorrect.

### Expected Behavior

The Mongolian currency's correct spelling is "Mongolian Tugrik" (as supported by the Bank of Mongolia and other major financial institutions).

### Current Behavior

The Mongolian currency (MNT) is currently named "Mongolian Tugrig" in the codebase.

### Affected Components

The incorrect spelling appears in the following files:
- packages/core/utils/src/defaults/currencies.ts — name: "Mongolian Tugrig" and name_plural: "Mongolian Tugrugs"
- packages/admin/dashboard/src/lib/data/currencies.ts — name: "Mongolian Tugrig"
- packages/plugins/loyalty/src/admin/lib/currencies.ts — name: "Mongolian Tugrig"

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
