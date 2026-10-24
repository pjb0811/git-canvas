## Status

The repository is in early planning: only `README.md` exists, with no source, package or tooling yet. Add sections here for commands, structure and release once they exist.

## Comments

Write comments for someone reading the code now: say what the code does first, give a reason only when the code alone would invite the wrong change (as a present-tense constraint), and replace history with an issue number such as `(#N)`. The full rules and examples are in section "C. 주석 작성" of the shared `coding-style` skill.

## Shared skills

Procedures shared by every pjb0811 repository are global Claude Code skills in the public repository [`pjb0811/skills`](https://github.com/pjb0811/skills), and the shared decisions are in its [`global/CLAUDE.md`](https://github.com/pjb0811/skills/blob/main/global/CLAUDE.md). Agents without them installed follow the summaries in this file.

| Skill                                 | Use                                                                                                                                                                            |
| ------------------------------------- | ------------------------------------------------------------------------------------------------------------------------------------------------------------------------------ |
| `commit`, `pr`, `issue`               | Commit messages, PR and issue bodies                                                                                                                                           |
| `coding-style`                        | Conventions, renames, comments (C), boolean names (D), braces (E), subcomponent file layout (F), blank lines (G), order of code inside a component (H), feature subfolders (I) |
| `changesets-release`, `publish-check` | Release flow and pre-release checks                                                                                                                                            |
| `shared-library-first`                | Reusable UI goes to ui-kit and hooks to use-hooks first                                                                                                                        |
| `ref-verification`                    | Read repository state from git refs, not the worktree                                                                                                                          |
| `repo-settings`                       | Align the repository's GitHub settings (merge methods, auto-merge, default-branch ruleset) with the standard                                                                   |

### Commit messages

- `type(scope): summary`: English imperative, lowercase start, no period, no gitmoji.
- Add a scope only when the change stays in one area. Never use the branch name.
- A breaking change puts `!` after the type or scope (`refactor(api)!: …`).
- The body is `-` bullets saying concretely what changed; for a breaking change, what breaks and what replaces it.
- No trailers such as `Co-Authored-By`.
