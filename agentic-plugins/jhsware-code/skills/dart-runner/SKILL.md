---
name: dart-runner
description: Run dart-runner tool to perform development tool actions such as building, testing and linting while limiting token usage.
allowed-tools:
  - mcp__jhsware_code_filesystem__filesystem
  - mcp__jhsware_code_dart_runner__dart-runner
disallowed-tools:
  - Bash
  - Read
  - Write
  - Edit
model: sonnet
context: fork
---

Run the dart-runner tool and provide a summary of the result so a calling skill or agent can decide how to proceed.