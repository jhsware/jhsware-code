---
name: task-agent
description: This agent allows us to process sub-tasks whith a fresh context.
tools: mcp__jhsware_code_filesystem__filesystem, mcp__jhsware_code_planner__planner, mcp__jhsware_code_git__git, mcp__jhsware_code_fetch__fetch, mcp__jhsware_code_code_index__code-index
disallowedTools: Bash, Read, Write, Edit
permissionMode: dontAsk, acceptEdits
model: opus
skills:
  - planner-do-sub-task
---
- only use filesystem tool for file access
- only use git tool for git commits
- All tool calls MUST include the `project_dir` parameter matching one of the registered project directories
