# OMP install and agent exposure verification

Fresh verification run after the raw-source audit update.

## Environment

- Repository under test: `/home/dmytro/dmltdev/plugins/agent-roles`
- Clean temporary OMP home: `/tmp/agent-roles-final-omp-qcU9X8`

## Commands and observed results

| Command | Exit | Observed result |
|---|---:|---|
| `HOME=/tmp/agent-roles-final-omp-qcU9X8 omp plugin marketplace add /home/dmytro/dmltdev/plugins/agent-roles` | 0 | `✔ Added marketplace: /home/dmytro/dmltdev/plugins/agent-roles` |
| `HOME=/tmp/agent-roles-final-omp-qcU9X8 omp plugin discover agent-roles` | 0 | Shows `agent-roles@0.1.0` with the plugin description. |
| `HOME=/tmp/agent-roles-final-omp-qcU9X8 omp plugin install agent-roles@agent-roles --force` | 0 | `✔ Installed agent-roles from agent-roles (0.1.0)` |
| `HOME=/tmp/agent-roles-final-omp-qcU9X8 omp plugin list` | 0 | Shows `agent-roles@agent-roles (0.1.0) (user)`. Project plugins from the parent checkout also appear. |
| `HOME=/tmp/agent-roles-final-omp-qcU9X8 omp plugin doctor` | 0 | `Summary: 2 ok, 1 warnings, 0 errors`; warning is `package_manifest: Not created yet` in the clean temporary home. |

## Installed agent files

OMP installed the plugin into:

```text
/tmp/agent-roles-final-omp-qcU9X8/.omp/plugins/cache/plugins/agent-roles___agent-roles___0.1.0
```

The installed plugin cache contains all six expected root `agents/*.md` files with `name` and `description` frontmatter:

| Agent file | Frontmatter name |
|---|---|
| `agents/product-architect.md` | `product-architect` |
| `agents/systems-architect.md` | `systems-architect` |
| `agents/principal-engineer.md` | `principal-engineer` |
| `agents/verification-lead.md` | `verification-lead` |
| `agents/security-architect.md` | `security-architect` |
| `agents/delivery-lead.md` | `delivery-lead` |

OMP agent discovery documentation says extension packages are searched at `<extension-root>/agents`, so these installed root `agents/*.md` definitions are in the plugin discovery location.

## Dispatch probe

A minimal dispatch probe was attempted from the same clean temporary OMP home:

```bash
HOME=/tmp/agent-roles-final-omp-qcU9X8 omp --plugin-dir /home/dmytro/dmltdev/plugins/agent-roles --no-session --max-time 20 -p 'Use product-architect to list only its role name.'
```

Observed result:

```text
No models available. Use /login or set an API key environment variable. Then use /model to select a model.

Set an API key environment variable:
  ANTHROPIC_API_KEY, OPENAI_API_KEY, GEMINI_API_KEY, etc.

Or create /tmp/agent-roles-final-omp-qcU9X8/.omp/agent/models.yml
```

Dispatch was not completed because the clean temporary OMP home had no model credentials or `models.yml`. The install/discover/list/cache checks above are the available clean-home proof that the plugin installs and exposes all six agent definition files at OMP's documented extension agent path.
