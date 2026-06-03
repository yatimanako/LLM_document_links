# Claude Harness Design

As of this moment, Anthropic has not published any standalone document that officially defines “Harness.”
However, the concept, design philosophy, and construction methods of a harness are described across the following two official resources.
  1. Configure your environment section in Best practices for Claude Code
  2. Harness design for long‑running application development

---
## 1. Components of Harness (Configure your environment)

### 📌 Document Link

[https://code.claude.com/docs/en/best-practices#configure-your-environment](https://code.claude.com/docs/en/best-practices#configure-your-environment)

### 📝 Summary
The document outlines how to build a robust, extensible harness that enables Claude to work effectively with codebase. It covers creating a clear **CLAUDE.md** to guide the model, setting proper **permissions**, and using **CLI tools** for efficient workflows. Also it describes connecting **MCP servers**, adding **hooks**, and defining **skills** to extend Claude’s capabilities. Advanced customization is supported through **custom subagents** and optional **plugins** that enhance automation and reasoning.

Overall, the document provides a blueprint of Harness for configuring a powerful, modular development environment around Claude Code.

### 🔍 Key Takeaways
- CLAUDE.md
  - Ask “Would removing this cause Claude to make mistakes?”. If not, cut it.
  - Tune instructions by adding emphasis (e.g., “IMPORTANT” or “YOU MUST”) to improve adherence.
- Permission
  - There are three ways to reduce interruptions for permission requests by Claude: Auto mode, Permission Allowlists, and Sandboxing.
- Hooks
  - Claude can write hooks with prompts like “Write a hook that runs eslint after every file edit” or “Write a hook that blocks writes to the migrations folder.”
- Subagents
  - Tell Claude to use subagents explicitly: “Use a subagent to review this code for security issues.”

### 📚 Notes
- t.b.d.

---
## 2. Harness design for long‑running application development

### 📌 Document Link
[https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview](https://www.anthropic.com/engineering/harness-design-long-running-apps)

### 📝 Summary
Long‑running autonomous coding agents require deliberate harness design to avoid context loss and self‑evaluation bias. By introducing a multi‑agent structure—planner, generator, and evaluator—they achieved more coherent, higher‑quality outputs across multi‑hour builds. The evaluator, inspired by GAN‑style critique, proved essential for both subjective tasks like frontend design and objective tasks like full‑stack development. As models improved (e.g., Opus 4.6), some scaffolding became unnecessary, but evaluators still added value at the edge of model capability.

### 🔍 Key Takeaways
- Multi‑hour autonomous coding breaks down without structured harnesses due to context drift and self‑evaluation bias.
- A GAN‑inspired multi‑agent system (planner, generator, evaluator) significantly improves output quality.
- Explicit grading criteria make subjective tasks like frontend design reliably evaluable.
- Evaluators using real interaction tools (e.g., Playwright) catch bugs and enforce quality in full‑stack builds.
- As models advance, harness complexity must be re‑examined—some parts can be removed, others become newly valuable

### 📚 Notes
- t.b.d.
