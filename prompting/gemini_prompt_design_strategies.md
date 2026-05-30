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
  - Put your image first for single-image prompts. Prompts containing a single image (or video) might perform better if that is placed before the text prompt.
  - Break it down step-by-step
    ```
    1. First, count how many toilet paper rolls are in this picture.
    2. Then, determine how much toilet paper a typical person uses per day.
    3. Calculate how long these rolls of toilet paper will last.
    ```
    
- Image Generation Prompting
  - Start by thinking of your subject, context, and style. In the following example, style is 'sketch', subject is 'modern apartment building', and context is 'surrounded by skyscrapers'.
    ```
    Generate a sketch of a modern apartment building surrounded by skyscrapers.
    ```
    
  - In case of adding text in images, Use the following guidance to get the most out of this feature.
    - Keep it short: Limit text to 25 characters or less for optimal generation.
    - Multiple phrases: Experiment with two or three distinct phrases to provide additional information. Avoid exceeding three phrases for cleaner compositions.
    ```
    A poster with the text "Summerland" in bold font as a title, underneath this text is the slogan "Summer never felt so good"
    ```

- Video Generation Prompting
  - t.b.d. 
