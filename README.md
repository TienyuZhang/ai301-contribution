# Contribution 1: Incorrect spelling for the Mongolian currency name

**Contribution Number:** 1  

**Student:** Tienyu Zhang 

**Issue:** https://github.com/kubedoio/rustchat/issues/92

**Status:** Phase I Complete

---

## Why I Chose This Issue

I have hands-on experience with backend input validation — both at AWS and in my TCP server project — so this issue felt like a natural fit. It's also well-scoped with a clear goal: add missing tests for a specific code path. The risk/standard tag signals a straightforward, unambiguous change, making it an ideal first contribution to learn the codebase before tackling more complex issues.

---

## Understanding the Issue

### Problem Description

The channel creation API endpoint has no test coverage for invalid inputs (empty strings, illegal characters, names exceeding length limits), leaving the validation logic unverified and prone to silent regressions.

### Expected Behavior

The backend returns a 400 Bad Request with a descriptive error message for any invalid channel name, and no channel is created. These cases are covered by automated tests in CI.

### Current Behavior

No backend tests exist for invalid channel name inputs, so there is no automated guarantee the API correctly rejects malformed values.

### Affected Components

- Channel creation endpoint — the POST /channels route handler where validation should be enforced
- Validation logic — model-level or middleware input checks for channel name constraints
- Backend test suite — where the new test cases will be added
- CI pipeline — ensures the validation contract is protected on every future PR

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
