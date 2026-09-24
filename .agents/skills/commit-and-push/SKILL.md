---
name: commit-and-push
description: Commit and push changes the user has already reviewed and approved. Use when the user wants to save approved changes in Git and push them, with help choosing the commit scope and title.
---

# Commit and push

The user has already reviewed the changes. Complete the Git workflow without another code review, code edits, or test run unless requested.

## Choose the scope

- Inspect the repository status, current branch, staged diff, and push destination. Read the relevant diff only to understand the commit scope and write an accurate title.
- Use staged changes when present, preserving any partially staged files and leaving unstaged changes out.
- If nothing is staged, ask which changes to include unless the user has already specified the scope. Show the changed files and offer clear choices. Stage only the selected files or hunks.
- If there are no changes to commit, say so. Push existing unpushed commits only when they are within the user's requested scope.

## Choose the title

- Suggest a short, plain, imperative title describing the actual change, such as “Add TL;DR summarization skill.” Use a repository-required format or the user's preferred convention when provided.
- Show the included files and proposed title. Use the available structured question tool to let the user accept or edit the title before committing. If the user already supplied a title or authorized automatic title selection, use that instruction without asking again.
- Prefer the GUI question box for scope and title choices, with concise options and a recommended choice. If that tool is unavailable, ask in chat. Wait for an answer when the choice is required; a preselected option is not an answer.

## Commit and push

- Verify that the staged diff still matches the selected scope, then create the commit with the agreed title. Do not amend an existing commit unless explicitly requested.
- Push to the current branch's configured destination. Before pushing, check whether this would also publish earlier commits; ask about any additional commits outside the agreed scope.
- If the branch has no push destination, suggest a destination using the repository's remotes and ask the user to choose or confirm it. If the repository is in a detached HEAD state, ask which branch to use before committing.
- If conflicts, hooks, authentication, or a rejected push block progress, report the concrete problem and request the needed decision or access. Do not bypass hooks, force push, reset, rebase, or merge automatically.
- Do not create a pull request or merge branches as part of this skill.
- Finish with the commit title, short hash, and push result, including the destination branch. If the commit succeeded but the push failed, clearly distinguish those outcomes.
