# Claude Prompt Engineering

## 📌 Document Link
https://platform.claude.com/docs/en/build-with-claude/prompt-engineering/overview

## 📝 Summary
A high‑level guide to designing effective prompts for Claude models.  
Covers structured prompting, role assignment, and multi‑step reasoning.

## 🔍 Key Takeaways
- Use clear task instructions and constraints.
- Break complex tasks into steps.
- Provide examples when possible.
- Prefer structured formats (bullet points, XML, JSON).

## 📚 Notes
- Best Practices
  - Use examples effectively with tags. Examples are one of the most reliable ways to steer Claude's output format, tone, and structure.
      ```
      You are an expert technical assistant. 
      Rewrite the following text to be more concise and professional.
        {{input_text}}
      
      <example>
        <input>
          The system architecture is kind of complicated and has many parts working together.
        </input>
        <output>
          The system architecture consists of multiple integrated components that operate cohesively.
        </output>
      </example>
      ```
  - Add context to improve performance. It helps Claude better understand goals and deliver more targeted responses.
      ```
      Your response will be read aloud by a text-to-speech engine, so never use ellipses since the text-to-speech engine will not know how to pronounce them.
      ```
  - Put longform data at the top. This helps Claude cut through the noise of the rest of the document's contents.
      ```
      <documents>
        <document index="1">
          <source>annual_report_2023.pdf</source>
          <document_content>
            {{ANNUAL_REPORT}}
          </document_content>
        </document>
        <document index="2">
          <source>competitor_analysis_q2.xlsx</source>
          <document_content>
            {{COMPETITOR_ANALYSIS}}
          </document_content>
        </document>
      </documents>
      
      Analyze the annual report and competitor analysis. Identify strategic advantages and recommend Q3 focus areas.
      ```
  - Give Claud a role.
      ```Python
      message = client.messages.create(
        model="claude-opus-4-7",
        max_tokens=1024,
        system="You are a helpful coding assistant specializing in Python.",
        messages=[
          {"role": "user", "content": "How do I sort a list of dictionaries by key?"}
        ],
      )
      ```
