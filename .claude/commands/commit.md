# Commit Changes

Stage, commit, and push changes to the repository.

## Process

1. **Review Changes**
   - Run `git status` to see all modified and untracked files
   - Run `git diff` to review the actual changes
   - Identify what was changed and why

2. **Stage Relevant Files**
   - Add files that represent a coherent change
   - Don't stage unrelated changes together
   - Never stage files containing secrets (.env, credentials, etc.)

3. **Generate Commit Message**
   - Summarize the nature of the changes (new feature, update, fix, docs, etc.)
   - Focus on the "why" rather than the "what"
   - Keep it concise (1-2 sentences)
   - Match the repository's commit style

4. **Commit and Push**
   - Create the commit
   - Push to remote
   - Verify success with `git status`

## Commit Message Guidelines

- **Add**: Wholly new content or feature
- **Update**: Enhancement to existing content
- **Fix**: Correction or bug fix
- **Remove**: Deletion of content
- **Refactor**: Reorganization without changing meaning

## Important Rules

- Do NOT include AI attribution lines (no "Generated with Claude Code" or "Co-Authored-By")
- Use a HEREDOC for commit messages to ensure proper formatting
- Never force push to main
- If there are no changes, don't create an empty commit

## Optional Arguments

$ARGUMENTS

If a specific commit message is provided, use it. Otherwise, generate an appropriate message based on the changes.
