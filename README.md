# Renovate reproduction repo: not poetry updates for `^1.2.3.0` (caret + four components)

```toml
[tool.poetry.dependencies]
python = "^3.11"
types-setuptools = "^69.0.0.20240115"
types-pytz = ">= 2023.3.1.0"
```

Renovate only detects and provides updates for `types-pytz`: both have four components,
caret contraints do not work, inequality does work.

The two DependaBot PRs show that both dependencies are out-of-date.

Sadly, caret contraints are the default: they are used when just running:

```sh
poetry add types-X
```

Upstream discussion: https://github.com/renovatebot/renovate/discussions/26939
