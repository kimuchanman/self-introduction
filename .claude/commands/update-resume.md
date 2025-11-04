---
description: Update docs/README.md with latest commits and PRs from specified repositories
---

# Update Resume Task

You are tasked with updating the professional resume document (docs/README.md) with the latest contributions from specified repositories.

## Usage

The user will provide repository paths as arguments. For example:
```
/update-resume ../xuan ../xuan-mcp-servers
```

If no arguments are provided, ask the user which repositories to collect from.

## Collection Process

For each repository provided, collect:
- All commits by the current git user (use `git config user.name`)
- All PRs authored by the current user (use `gh pr list --author=@me --state=all --limit=100`)

Use the following commands for each repository:
```bash
cd <REPO_PATH> && git log --author="$(git config user.name)" --oneline --no-merges
cd <REPO_PATH> && gh pr list --author=@me --state=all --limit=100 --json number,title,state,mergedAt,createdAt,url
```

## Update Guidelines

1. **Read the current docs/README.md** to understand the existing structure
2. **Identify the appropriate section** to update (typically the most recent work period)
3. **Add new achievements** based on collected commits and PRs
4. **DO NOT include**:
   - Specific internal package names
   - Direct PR links or commit hashes
   - Internal repository names
   - Internal-only information
5. **DO include**:
   - General technical achievements
   - Technologies used
   - Impact and outcomes
   - Quantifiable results where possible

## Document Structure

The resume is a public-facing document. Typically update the most recent work period section.

### Common Categories for Updates

Organize updates into relevant categories such as:
- Visual Regression Testing (VRT) 基盤の改善
- Feature Flag 基盤の強化
- CI/CD ワークフローの最適化
- コード品質と DX 向上
- モノレポ最適化
- アーキテクチャとナビゲーション基盤の改善
- AI/自動化ツールの導入と生産性向上
- その他の開発基盤改善

### Technology Stack

Update the technology stack list with any new tools or technologies used.

## Output Format

- Use bullet points for achievements
- Keep descriptions concise but informative
- Focus on impact and value delivered
- Use Japanese for all content
- Maintain consistency with existing writing style

## Important Notes

- This is a **public-facing document** - do not expose internal details
- Focus on **technical achievements and skills** rather than specific implementation details
- Ensure all information is **anonymized** and **generalized** where necessary
- The document should showcase professional growth and technical expertise
- Repository names provided by the user should NOT appear in the final document

## Task Workflow

1. Create a todo list for tracking progress
2. Collect commits and PRs from each specified repository
3. Read and understand the current docs/README.md structure
4. Update docs/README.md with generalized technical achievements
5. Mark tasks as completed as you progress
