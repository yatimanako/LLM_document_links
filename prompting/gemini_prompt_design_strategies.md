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
  - Include the follwing items.
    - Subject: The object, person, animal, or scenery that you want in your video, such as cityscape, nature, vehicles, or puppies.
    - Action: What the subject is doing (for example, walking, running, or turning their head).
    - Style: Specify creative direction using specific film style keywords, such as sci-fi, horror film, film noir, or animated styles like cartoon.
    - Camera positioning and motion: (Optional) Control the camera's location and movement using terms like aerial view, eye-level, top-down shot, dolly shot, or worms eye.
    - Composition: (Optional) How the shot is framed, such as wide shot, close-up, single-shot or two-shot.
    - Focus and lens effects: (Optional) Use terms like shallow focus, deep focus, soft focus, macro lens, and wide-angle lens to achieve specific visual effects.
    - Ambiance: (Optional) How the color and light contribute to the scene, such as blue tones, night, or warm tones.
   
  - Examples
    - Subject and Context
      ```
      An architectural rendering of a white concrete apartment building with flowing organic shapes, seamlessly blending with lush greenery and futuristic elements
      ```

    - Action
      ```
      A wide shot of a woman walking along the beach, looking content and relaxed towards the horizon at sunset.
      ```

    - Style
      ```
      Film noir style, man and woman walk on the street, mystery, cinematic, black and white.
      ```

    - Camera motion and composition
      ```
      A POV shot from a vintage car driving in the rain, Canada at night, cinematic.
      ```

    - Ambiance
      ```
      A close-up of a girl holding adorable golden retriever puppy in the park, sunlight.
      ```

    - Aspect ratios
      ```
      Widescreen (16:9)
      Create a video with a tracking drone view of a man driving a red convertible car in Palm Springs, 1970s, warm sunlight, long shadows.
      ```
