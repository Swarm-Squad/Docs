---
outline: deep
---

# Getting Started with Swarm Squad Episode I

Welcome to Swarm Squad Episode I: Surviving the Jam, a specialized simulation framework focusing on hybrid control architecture for autonomous multi-agent systems in communication-challenged environments.

## What is Swarm Squad Episode I?

Swarm Squad Episode I is a research-focused simulation framework that explores how multi-agent systems can maintain coordination and achieve objectives when communication is disrupted or jammed. The framework features:

- 🤖 **Hybrid Control Architecture**: Combines behavior-based and formation control approaches
- 📡 **Communication Jamming Simulation**: Models realistic communication disruptions
- 🧠 **LLM Integration**: Incorporates Large Language Models for high-level decision making
- 🎯 **Formation Control**: Advanced algorithms for maintaining swarm formations
- 🔄 **Adaptive Behavior**: Agents that can adapt to changing communication conditions
- 📊 **Real-time Visualization**: Interactive GUI for monitoring swarm behavior
- 🔬 **Research-Oriented**: Built for academic research and experimental studies

## Quick Start

For most users, getting started with Swarm Squad Episode I is as simple as:

```bash
# Install Swarm Squad Episode I
uv pip install swarm-squad-ep1

# Run the application
swarm-squad-ep1
swarm-squad-ep1 --help
```

That's it! The application will start and you can begin exploring communication-challenged multi-agent systems.

## Prerequisites

For basic usage, you only need:

- **[uv](https://docs.astral.sh/uv/getting-started/installation/)**: For package installation and management (recommended)

### Installing uv

If you don't have uv installed, you can install it using:

```bash
# macOS/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## Installation

### Option 1: Install from PyPI (Recommended)

The simplest way to install Swarm Squad Episode I is directly from PyPI:

```bash
# Install the package using uv
uv pip install swarm-squad-ep1
```

### Option 2: Development Installation

For contributors, developers, or if you plan to modify the framework:

**Additional Prerequisites for Development:**

- **[git](https://git-scm.com/downloads)**: For cloning the repository
- **[ruff](https://docs.astral.sh/ruff/)**: For code linting and formatting
- **[pre-commit](https://pre-commit.com/)**: For code quality hooks

```bash
# Clone the repository
git clone https://github.com/Sang-Buster/Swarm-Squad-Ep1
cd Swarm-Squad-Ep1

# Option 1 (Recommended): Synchronize environment with dependencies
uv sync
source .venv/bin/activate  # On Linux/macOS
# Or: .venv\Scripts\activate  # On Windows

# Option 2 (Manual): Create virtual environment manually
uv venv --python 3.10
source .venv/bin/activate  # On Linux/macOS
# Or: .venv\Scripts\activate  # On Windows
uv pip install -e .
```

## Running Swarm Squad Episode I

After installation, you can run Swarm Squad Episode I using the command-line interface:

```bash
# Run with default settings
swarm-squad-ep1

# Show available options and help
swarm-squad-ep1 --help
```

## Development Setup

If you're planning to develop or extend Swarm Squad Episode I, set up the development environment:

### Install Development Tools

```bash
# Install development dependencies
uv pip install ruff pre-commit
```

### Set up Git Hooks

```bash
# Install git hooks for code quality
pre-commit install --install-hooks
```

These hooks perform different checks at various stages:

- **`commit-msg`**: Ensures commit messages follow the conventional format
- **`pre-commit`**: Runs Ruff linting and formatting checks before each commit
- **`pre-push`**: Performs final validation before pushing to remote

### Code Quality Checks

```bash
# Run linting and formatting
ruff check --fix
ruff check --select I --fix
ruff format
```

### Running from Source

When developing, you can run directly from the source code:

```bash
uv run src/swarm_squad_ep1/main.py
```

## Project Structure

Understanding the Swarm Squad Episode I file structure will help you navigate and extend the framework:

```
📂 Swarm Squad Episode I
┣ 📂 src/swarm_squad_ep1/      # Main source code
┃ ┣ 📂 controllers/            # Control system implementations
┃ ┃ ┣ 📄 base_controller.py    # Base controller interface
┃ ┃ ┣ 📄 behavior_controller.py # Behavior-based control
┃ ┃ ┣ 📄 formation_controller.py # Formation control algorithms
┃ ┃ ┣ 📄 llm_controller.py     # LLM integration for decision making
┃ ┃ ┗ 📄 controller_factory.py # Controller management
┃ ┣ 📂 models/                 # Data models and state management
┃ ┃ ┗ 📄 swarm_state.py        # Swarm formation state
┃ ┣ 📂 gui/                    # Graphical user interface
┃ ┃ ┗ 📄 formation_control_gui.py # Main GUI implementation
┃ ┣ 📂 config/                 # Configuration files
┃ ┃ ┗ 📄 config.py             # Simulation parameters
┃ ┗ 📄 main.py                 # Application entry point
┣ 📂 lib/                      # Supplementary materials
┃ ┣ 📂 papers/                 # Research papers
┃ ┣ 📂 presentations/          # Slides and presentations
┃ ┗ 📂 simulations/            # Original simulation results
┣ 📄 pyproject.toml            # Project configuration
┗ 📄 uv.lock                   # Dependency lock file
```

## Key Components

Swarm Squad Episode I includes several specialized components for communication-challenged environments:

### Controllers

Located in `src/swarm_squad_ep1/controllers/`, these implement different control strategies:

- **`base_controller.py`**: Defines the interface for all controllers
- **`behavior_controller.py`**: Implements behavior-based control algorithms
- **`formation_controller.py`**: Handles formation control and maintenance
- **`llm_controller.py`**: Integrates Large Language Models for high-level decision making
- **`controller_factory.py`**: Manages controller instantiation and selection

### Models

Located in `src/swarm_squad_ep1/models/`:

- **`swarm_state.py`**: Manages the state of the swarm formation and agent positions

### GUI

Located in `src/swarm_squad_ep1/gui/`:

- **`formation_control_gui.py`**: Provides real-time visualization and user interaction

## Simulation Configuration

The simulation behavior can be configured through parameters in `src/swarm_squad_ep1/config/config.py`, including:

- **Formation Settings**: Define swarm formation parameters and constraints
- **Communication Parameters**: Configure communication range and reliability
- **Jamming Simulation**: Set up communication disruption scenarios
- **Visualization Options**: Customize the GUI appearance and behavior
- **LLM Integration**: Configure language model parameters and endpoints

## First Simulation

Once you have Swarm Squad Episode I installed, you can run your first simulation:

1. **Launch the Application**:

   ```bash
   swarm-squad-ep1
   ```

2. **Explore the GUI**: The interface provides:

   - Real-time swarm visualization
   - Formation control parameters
   - Communication status indicators
   - Performance metrics dashboard

3. **Run Scenarios**: Test different communication jamming scenarios to observe adaptive behavior

## Supplementary Materials

For more in-depth understanding, refer to the supplementary materials in the `lib` directory:

- **Research Papers**: Detailed theoretical background and methodology
- **Presentation Slides**: Visual explanations of key concepts and results
- **Original Simulations**: Implementation details and experimental results

## Next Steps

Now that you have Swarm Squad Episode I installed and running, explore these areas:

1. **[Architecture](./architecture.md)**: Understand the hybrid control system design
2. **[Configuration](./configuration.md)**: Learn about simulation parameters and customization
3. **[Demo](./demo.md)**: Try out example scenarios and use cases
4. **Research Integration**: Explore the academic papers and experimental results

## Troubleshooting

If you encounter issues during installation or setup:

### Common Issues

- **Python Version**: Ensure you're using Python 3.10 or higher
- **Virtual Environment**: Always work within a virtual environment to avoid conflicts
- **Dependencies**: Run `uv pip install -e .` again if you encounter import errors
- **GUI Issues**: Ensure you have the necessary graphics libraries installed

### Getting Help

- Check the error messages for specific guidance
- Review the logs in the terminal output
- Ensure all prerequisites are correctly installed
- Visit the project's GitHub repository for issue tracking and community support

With Swarm Squad Episode I properly installed and configured, you're ready to explore adaptive multi-agent systems in communication-challenged environments!
