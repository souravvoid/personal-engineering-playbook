# Optional AI/ML guidelines

AI/ML is not the default. Use it only when it provides a defensible benefit over simpler logic.

## Problem and data
- Define the prediction/generation task, intended users, inputs, outputs, baseline, evaluation metric, and cost of failure.
- Check data provenance, permission, licensing, privacy, representativeness, class imbalance, and leakage.
- Keep train/validation/test data separated correctly.

## Model evaluation
- Establish a non-ML baseline.
- Evaluate on held-out data using metrics appropriate to the task.
- Report dataset scope, metric, threshold, limitations, and failure cases.
- Do not invent accuracy or present confidence as certainty.
- Handle low-confidence, malformed, and out-of-distribution inputs safely.

## LLM applications
- Consider prompt injection, data exfiltration, hallucination, tool permissions, cost, latency, and provider outages.
- Treat retrieved documents and user-provided content as untrusted data, not instructions.
- Restrict tools to the minimum required permissions.
- Avoid sending sensitive data to external providers without an explicit design decision.
- Provide fallbacks and communicate uncertainty.

## Architecture
Keep inference behind backend boundaries when secrets, authorization, or model assets require it. Separate data preparation, training/evaluation, and inference. Record model/version and relevant configuration.
