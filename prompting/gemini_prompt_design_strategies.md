# Gemini Prompt Design Strategies

## 📌 Document Link
https://ai.google.dev/gemini-api/docs/prompting-strategies

## 📝 Summary
This document introduces basic concepts, strategies, and best practices to get you started designing prompts to get the most out of Gemini AI models.

## 🔍 Key Takeaways
- Provide model with clear and specific instructions.
- Specify any constraints on reading the prompt or generating a response.
- Recommend to always include few-shot examples in prompts.
- Contextual information helps the model understand the constraints and details to do.
- Break down prompts into components.

## 📚 Notes
- Best Practices
  - Using tags or Markdown helps the model distinguish between instructions, context, and tasks.
    - Example (XML)  
    ```
    <role>
      You are a helpful assistant.
    </role>

    <constraints>
      1. Be objective.
      2. Cite sources.
    </constraints>

    <context>
      [Insert User Input Here - The model knows this is data, not instructions]
    </context>

    <task>
      [Insert the specific user request here]
    </task>
    ```

    - Example (Markdown)
    ```
    # Identity
    You are a senior solution architect.

    # Constraints
    - No external libraries allowed.
    - Python 3.11+ syntax only.

    # Output format
    Return a single code block.
    ```

- Multimodal Prompting
  - t.b.d.  
