# Self-use build

This branch is a personal build maintained by [@Momoyeyu](https://github.com/Momoyeyu),
based on [MeteorNOX/DeepSeek-Balance-Whale-Widget](https://github.com/MeteorNOX/DeepSeek-Balance-Whale-Widget)
(MIT licensed; see `LICENSE` and the original README).

It exists so the local DSH Desktop profile can use one branch that contains our
open fixes without waiting for upstream merges:

- `fix/client-module-lifecycle` — PR #270: manage the widget client through
  `dsh.client` so disabling/enabling the bundle takes effect (disable reloads
  once; enable is live).
- `fix/bubble-text-fit` — PR #272 (Refs #159): fit the bubble text inside the
  ellipse after render; row padding/radius scale with `--dshwv-u`.

Upstream is kept as the `origin` remote, so this branch can be refreshed with:

```bash
git fetch origin
git merge origin/main
```

The local Desktop profile links to this checkout directly:

```text
~/.dsh/profiles/desktop/node_modules/dsh-whale-widget -> this checkout
```

Nothing here changes the upstream contribution branches; they remain separate
and PR-sized.
