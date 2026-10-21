---
name: flutter-runner
description: Run flutter-runner tool to perform development tool actions such as building, testing and linting while limiting token usage.
allowed-tools:
  - mcp__jhsware_code_filesystem__filesystem
  - mcp__jhsware_code_flutter_runner__flutter-runner
disallowed-tools:
  - Bash
  - Read
  - Write
  - Edit
model: sonnet
context: fork
---

Run the flutter-runner tool and provide a summary of the result so a calling skill or agent can decide how to proceed.