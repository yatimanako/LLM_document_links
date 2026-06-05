# Harness Engineering for Codex

## 📌 Document Link
[Harness engineering: leveraging Codex in an agent-first world](https://openai.com/index/harness-engineering/)

## 🔍 Key Takeaways
- **The team built an entire internal software product with zero manually written code**, relying entirely on Codex agents to generate application logic, tests, CI, documentation, and tooling
- **Engineers shifted from writing code to designing environments, constraints, and feedback loops** that enable agents to work reliably and autonomously
- **Repository legibility and structured, in‑repo knowledge became essential**, replacing large instruction files with a navigable, versioned documentation system that agents can reason over
- **Strict architectural rules and custom linters enforce consistency**, allowing agents to ship quickly without causing structural drift or accumulating unbounded technical debt
- **Codex reached near end‑to‑end autonomy**, able to reproduce bugs, implement fixes, validate behavior, open PRs, respond to feedback, and merge changes with minimal human intervention

## 📚 Notes
- Give Codex a map, not a 1,000-page instruction manual
- Instead of treating AGENTS.md as the encyclopedia, OpenAI team treated it as the table of contents
  - Example
    ```
    AGENTS.md
    ARCHITECTURE.md
    docs/
    ├── design-docs/
    │   ├── index.md
    │   ├── core-beliefs.md
    │   └── ...
    ├── exec-plans/
    │   ├── active/
    │   ├── completed/
    │   └── tech-debt-tracker.md
    ├── generated/
    │   └── db-schema.md
    ├── product-specs/
    │   ├── index.md
    │   ├── new-user-onboarding.md
    │   └── ...
    ├── references/
    │   ├── design-system-reference-llms.txt
    │   ├── nixpacks-llms.txt
    │   ├── uv-llms.txt
    │   └── ...
    ├── DESIGN.md
    ├── FRONTEND.md
    ├── PLANS.md
    ├── PRODUCT_SENSE.md
    ├── QUALITY_SCORE.md
    ├── RELIABILITY.md
    └── SECURITY.md
    ```

- Humans always remain in the loop, but work at a different layer of abstraction: prioritize work, translate user feedback into acceptance criteria, and validate outcomes
- Building software still demands discipline, but the discipline shows up more in the scaffolding rather than the code. The tooling, abstractions, and feedback loops that keep the codebase coherent are increasingly important
