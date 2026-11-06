---
name: planner-do-sub-task
description: "Perform a task as described in the task. Use planner to create a task to plan and track work."
allowed-tools:
  - mcp__jhsware_code_planner__planner
  - mcp__jhsware_code_filesystem__filesystem
  - mcp__jhsware_code_git__git
  - mcp__jhsware_code_fetch__fetch
  - mcp__jhsware_code_code_index__code-index
disallowed-tools:
  - Bash
  - Read
  - Write
  - Edit
model: opus
---

ultrathink

The task prompt contains two distinct sections:
- **Task context** — title, details (background, purpose, files, acceptance criteria). This is reference information.
- **`## Steps to perform`** — the numbered list of actual steps to execute. Only perform steps listed under this header.

When working on an ad hoc task:
- [ ] Step 1: Present an overview of the plan to the user
- [ ] Step 2: When the user is satisfied, create a plan for the appropriate project using planner
- [ ] Step 3: Work on the plan according to the steps below

When working on a task:
- [ ] Step 1: Set task status to started
- [ ] Step 2: Make sure we are on master and create a branch
- [ ] Step 3: Process each step individually
- [ ] Step 4: When all steps are done, set task to done
- [ ] Step 5: If coding task - offer to merge the branch
- [ ] Step 6: If coding task - when code is merged to master, set task to merged

When processing a step:
- [ ] Step 1: Set step status to started
- [ ] Step 2: Perform the step
- [ ] Step 3: If coding task - make sure you are on the correct branch and create logical commits
- [ ] Step 4: Use task memory to store context for later steps
- [ ] Step 5: When step is completed, mark step done

## Tool Reference

All tool calls MUST include the `project_dir` parameter matching one of the registered project directories. Omitting `project_dir` will return a validation error.

Use filesystem (jhsware_code_filesystem) to read, search and edit files.
Use git (jhsware_code_git) for git operations.
Use the agent runner-agent to run code test, analyze or build the project. Use runner-agent for flutter or dart code generation.

Do not use native tools: Bash, Read, Write, Edit, Git.
Do not delete files, ask user to delete them.
Do not run bash commands, ask user to do this.