# git-canvas

Presentational UI library for visualizing and interacting with git repositories — commit graphs, history, diffs, and commit/branch/merge actions.

`git-canvas` is a controlled-component library: it renders whatever git data it's given as props and emits callbacks for user actions (e.g. "create branch", "commit"), without performing any git operations, data fetching, or authentication itself. Consuming applications own the actual git engine (e.g. `isomorphic-git`, a backend, or the GitHub API) and feed data in / handle callbacks.

Status: early planning stage — no implementation yet.
