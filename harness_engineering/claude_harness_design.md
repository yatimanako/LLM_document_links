# Claude Harness Design

## 📌 Document Link
[https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview](https://www.anthropic.com/engineering/harness-design-long-running-apps)

## 📝 Summary
Long‑running autonomous coding agents require deliberate harness design to avoid context loss and self‑evaluation bias. By introducing a multi‑agent structure—planner, generator, and evaluator—they achieved more coherent, higher‑quality outputs across multi‑hour builds. The evaluator, inspired by GAN‑style critique, proved essential for both subjective tasks like frontend design and objective tasks like full‑stack development. As models improved (e.g., Opus 4.6), some scaffolding became unnecessary, but evaluators still added value at the edge of model capability.

## 🔍 Key Takeaways
- Multi‑hour autonomous coding breaks down without structured harnesses due to context drift and self‑evaluation bias.
- A GAN‑inspired multi‑agent system (planner, generator, evaluator) significantly improves output quality.
- Explicit grading criteria make subjective tasks like frontend design reliably evaluable.
- Evaluators using real interaction tools (e.g., Playwright) catch bugs and enforce quality in full‑stack builds.
- As models advance, harness complexity must be re‑examined—some parts can be removed, others become newly valuable

## 📚 Notes
