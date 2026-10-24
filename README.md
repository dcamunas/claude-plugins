# claude-plugins

The marketplace `dcamunas` for Claude Code: the catalogue of my plugins, each in its own repository.

```bash
claude plugin marketplace add dcamunas/claude-plugins
claude plugin install model-router@dcamunas   # the model and effort for every subagent, by risk
```

| Plugin | What it does | Repository |
|---|---|---|
| model-router | Picks the model and effort for every Claude Code subagent by its risk, and checks and escalates the work that needs it. | [dcamunas/model-router](https://github.com/dcamunas/model-router) |

Each plugin is pinned to a release tag and its commit. A new release reaches you only after this catalogue moves the pin, so a push to a plugin's `main` never lands on anyone's machine by itself.

MIT. See [LICENSE](LICENSE).
