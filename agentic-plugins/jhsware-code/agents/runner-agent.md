---
name: task-agent
description: This agent allows us to run development tool actions such as building, testing and analyzing code, while limiting token usage.
tools: filesystem, flutter-runner, dart-runner
disallowed-tools: Bash, Read, Write, Edit, Cowork
permission-mode: dontAsk, acceptEdits
model: sonnet
skills:
  - flutter-runner
  - dart-runner
---
- only use filesystem tool for file access
- All tool calls MUST include the `project_dir` parameter matching one of the registered project directories
