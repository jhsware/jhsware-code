---
name: task-agent
description: This agent allows us to process sub-tasks whith a fresh context.
tools: mcp__remote-devices__jhsware_code_filesystem-filesystem, mcp__remote-devices__jhsware_code_planner-planner, mcp__remote-devices__jhsware_code_git-git, mcp__remote-devices__jhsware_code_fetch-fetch, mcp__remote-devices__jhsware_code_code_index-code-index
disallowed-tools: Bash, Read, Write, Edit, Cowork
permission-mode: dontAsk, acceptEdits
model: opus
skills:
  - planner-do-sub-task
---
- only use filesystem tool for file access
- only use git tool for git commits
- All tool calls MUST include the `project_dir` parameter matching one of the registered project directories
