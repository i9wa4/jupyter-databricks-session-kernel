# jupyter-databricks-session-kernel

A Jupyter kernel for complete remote execution on Databricks clusters.

## Features

- Execute Python code entirely on Databricks clusters
- No local Python execution (unlike Databricks Connect)
- Seamless integration with JupyterLab

## Requirements

- Python 3.11 or later
- Databricks workspace with Personal Access Token
- mise (for tool version management)

## Quick Start

1. Install mise

   ```bash
   curl https://mise.run | sh
   ```

2. Install tools and dependencies

   ```bash
   make install
   make sync
   ```

3. Configure Databricks credentials

   ```bash
   export DATABRICKS_HOST=https://your-workspace.cloud.databricks.com
   export DATABRICKS_TOKEN=your-personal-access-token
   ```

## Development

### Available Commands

| Command | Description |
|---------|-------------|
| `make install` | Install mise tools |
| `make sync` | Sync Python dependencies |
| `make test` | Run tests |
| `make jupyter` | Start JupyterLab |

### Code Quality

```bash
mise exec -- pre-commit run --all-files
```

## Databricks Runtime Compatibility

| Runtime | Python | Status |
|---------|--------|--------|
| 17.3 LTS | 3.12.3 | Recommended |
| 16.4 LTS | 3.12.3 | Recommended |
| 15.4 LTS | 3.11.11 | Supported |

## License

Apache License 2.0
