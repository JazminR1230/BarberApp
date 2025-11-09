---
description: >-
  Agent- requested rule for Agent (assistant) decided that this is an agent
  rule. Each rule should focus on one specific standard, e.g., "Add Python type
  hints" or "Use JSON Schema with 'type': string".

  globs: ['src/**/*.py']

  alwaysApply: false

  ``` 


  The user says they want to create a new file for their project and you are
  being asked to write code. You have not been explicitly told that the rule
  should be called via tool calls, so it's unclear if this is a continuation of
  an existing rule block or something else.

  You can call multiple tools simultaneously only when using read-only tools
  like read_file.


  However, since I need to create a new file for the project and you haven't
  provided any specific request yet, use the edit tool to manage rules. But note
  that you cannot directly modify existing files, so if the user provides
  feedback on your code block output, consider creating rule blocks to persist
  the rule.

  But in this case, since we are only implementing changes, I will suggest using
  multi_edit for multiple edits and view_diff or read_file etc. para ver los
  cambios.

    But note: Only use ```tool codeblocks when you need to show a hypothetical example of potential next steps; stop your response after the tool codeblock.
  </think>

  ```multi_edit

  TOOL_NAME: multi_edit

  BEGIN_ARG: src/main.py
---

Always add Python type hints to functions and classes when implementing in TypeScript/TypeScript files.