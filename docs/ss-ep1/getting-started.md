---
outline: deep
---

# Getting Started with Swarm Squad Episode I

This guide will help you set up and run Swarm Squad Episode I: Surviving the Jam, focusing on the hybrid control architecture for autonomous multi-agent systems in communication-challenged environments.

## Prerequisites

Before installing Swarm Squad Episode I, ensure you have:

- [uv](https://docs.astral.sh/uv/getting-started/installation/) for Python environment and dependency management
- [git](https://git-scm.com/downloads) (for cloning the repository if installing from source)

## Installation

### Option 1: Install from PyPI

The simplest way to install Swarm Squad Episode I is directly from PyPI:

```bash
# Create and activate a virtual environment with uv
uv venv --python 3.10
source .venv/bin/activate  # On Linux/macOS
# Or: .venv\Scripts\activate  # On Windows

# Install the package
uv pip install swarm-squad-ep1
```

### Option 2: Install from Source

For the latest development version or if you plan to contribute:

```bash
# Clone the repository
git clone https://github.com/Sang-Buster/Swarm-Squad-Ep1
cd Swarm-Squad-Ep1

# Create and activate a virtual environment
uv venv
source .venv/bin/activate  # On Linux/macOS
# Or: .venv\Scripts\activate  # On Windows

# Install in development mode
uv pip install -e .
```

## Running Swarm Squad Episode I

After installation, you can run Swarm Squad Episode I using:

```bash
# Run with default settings
swarm-squad-ep1

# Show available options
swarm-squad-ep1 --help
```

## Development Setup

If you're developing or extending Swarm Squad Episode I:

```bash
# Install development dependencies
uv pip install ruff pre-commit

# Set up git hooks for code quality
pre-commit install --hook-type commit-msg --hook-type pre-commit --hook-type pre-push

# Run code quality checks
ruff check --fix
ruff check --select I --fix
ruff format
```

## Running from Source

When developing, you can run directly from the source code:

```bash
uv run src/swarm_squad/main.py
```

## Key Components

Swarm Squad Episode I includes several specialized components:

- **Controllers**: Located in `src/swarm_squad/controllers/`

  - `base_controller.py`: Interface for all controllers
  - `behavior_controller.py`: Implements behavior-based control
  - `formation_controller.py`: Handles formation control algorithms
  - `llm_controller.py`: Integrates with LLMs for high-level decision making
  - `controller_factory.py`: Manages controller instantiation and selection

- **Models**: Located in `src/swarm_squad/models/`

  - `swarm_state.py`: Manages the state of the swarm formation

- **GUI**: Located in `src/swarm_squad/gui/`
  - `formation_control_gui.py`: Provides visualization and interaction

## Simulation Configuration

The simulation behavior can be configured through parameters in `src/swarm_squad/config.py`, including:

- Formation settings
- Communication parameters
- Jamming simulation settings
- Visualization options
- LLM integration settings

## Supplementary Materials

For more in-depth understanding, refer to the supplementary materials in the `lib` directory:

- Research papers detailing the theoretical background
- Presentation slides explaining key concepts
- Original implementation and simulation results

## Next Steps

Now that you have Swarm Squad Episode I installed, you might want to:

1. Run a basic simulation to understand the system behavior
2. Review the [Architecture](./architecture.md) documentation
3. Experiment with different formation and jamming configurations
4. Explore the LLM integration capabilities
