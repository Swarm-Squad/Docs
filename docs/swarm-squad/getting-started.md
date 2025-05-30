---
outline: deep
---

# Getting Started with Swarm Squad

This guide will help you set up and run the Swarm Squad simulation framework on your system.

## Prerequisites

Before installing Swarm Squad, ensure that you have:

- [uv](https://docs.astral.sh/uv/getting-started/installation/) for Python environment and dependency management
- [git](https://git-scm.com/downloads) (for cloning the repository if installing from source)

## Installation

### Option 1: Install from PyPI

The simplest way to install Swarm Squad is directly from PyPI:

```bash
# Create and activate a virtual environment with uv
uv venv --python 3.10
source .venv/bin/activate  # On Linux/macOS
# Or: .venv\Scripts\activate  # On Windows

# Install the package
uv pip install swarm-squad
```

### Option 2: Install from Source

For the latest development version or if you plan to contribute:

```bash
# Clone the repository
git clone https://github.com/Sang-Buster/Swarm-Squad
cd Swarm-Squad

# Create and activate a virtual environment
uv venv --python 3.10
source .venv/bin/activate  # On Linux/macOS
# Or: .venv\Scripts\activate  # On Windows

# Install in development mode
uv pip install -e .
```

## Environment Setup

Swarm Squad requires some environment variables to be set for full functionality:

```bash
# Copy the example environment file
cp .env.example .env
```

You'll need to update the following variables in the `.env` file:

- `MAPBOX_ACCESS_TOKEN`: Get this by signing up at https://www.mapbox.com/
- `OLLAMA_API_URL`: Update if your Ollama instance is running at a different address
- `DATABASE_PATH`: Specify if you want to use a custom database file location

## Running Swarm Squad

After installation, you can run Swarm Squad using:

```bash
# Run with default settings
swarm-squad

# Show available options
swarm-squad --help
```

## Development Setup

If you're developing or extending Swarm Squad, you'll want to set up the development environment:

```bash
# Install development dependencies
uv pip install ruff pre-commit

# Set up git hooks for code quality
pre-commit install --hook-type commit-msg --hook-type pre-commit --hook-type pre-push

# Run code quality checks
ruff check
ruff check --fix
ruff check --select I
ruff check --select I --fix
ruff format
```

## Running from Source

When developing, you can run directly from the source code:

```bash
uv run src/swarm_squad/app.py
```

## Next Steps

Now that you have Swarm Squad installed, you might want to:

1. Check out the [Architecture](./architecture.md) documentation to understand how Swarm Squad is built
2. Explore the [Configuration](./configuration.md) options to customize your simulations
3. Run a demo simulation to see Swarm Squad in action

## Troubleshooting

If you encounter any issues:

- Ensure your Python version is 3.10 or higher
- Verify that all environment variables are set correctly
- Check that all dependencies were installed correctly
- See if there are any error messages that might indicate the source of the problem
