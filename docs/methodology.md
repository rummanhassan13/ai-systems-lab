# Methodology

How an experiment is run in this lab.

## 1. Define

Write the research question, the hypothesis, and acceptance criteria before writing code. If the result cannot change a decision, reconsider the experiment.

## 2. Build the smallest testable version

Prefer plain code and few dependencies. Every external service, model and library is recorded with its version.

## 3. Evaluate

- Use deterministic checks where possible (exact match, schema validation, retrieval recall).
- Use model-based judging only with a recorded rubric, judge prompt and judge model version.
- Keep evaluation data separate from any data used to tune prompts or parameters.
- Run enough repetitions to see variance, and report it.

## 4. Record

Use [`templates/experiment-report.md`](../templates/experiment-report.md). Report only numbers produced by committed scripts, with raw outputs linked. State dataset size and limitations next to each result.

## 5. Review before "Shipped"

An item moves to Shipped on the project board only when:

- [ ] Code and data are committed
- [ ] A reader can reproduce the main result from a clean clone
- [ ] Limitations and failures are documented
- [ ] References are cited
- [ ] No personal data, secrets or client content are present

## Safety and privacy

Use synthetic or public data. Logging of prompts and outputs is off by default, redacted when on, and has a retention limit. Tools with side effects require confirmation or run in a sandbox.