---
outline: deep
---

# Getting Started with Swarm Squad

Welcome to Swarm Squad, a comprehensive simulation framework for multi-agent systems. This guide will help you set up, configure, and run your first simulation with agent-based modeling capabilities.

## What is Swarm Squad?

Swarm Squad is a powerful simulation framework designed for multi-agent systems with the following key features:

- 🤖 **Agent Simulation**: Simulates multiple agents in a shared environment
- 📈 **Scalability**: Handles large-scale agent simulations efficiently
- ✅ **Behavior Specs**: Define and test agent behavior against expected outcomes
- 🌍 **Environment Modeling**: Build and manage physical or virtual environments
- 📊 **Analytics**: Collect metrics on speed, coordination, and performance
- ⚙️ **Customizable**: Easily extend agents, environments, and evaluation logic
- 🗺️ **Visualization**: Real-time views and post-run reports of simulations
- 🧰 **Tool Integration**: Connect with RL libraries, protocols, or visual tools
- 🚘 **Versatile Agents**: Supports robots, drones, and autonomous vehicles

## Quick Start

For most users, getting started with Swarm Squad is as simple as:

```bash
# Install Swarm Squad
uv pip install swarm-squad

# Run the application
swarm-squad
swarm-squad --help
```

That's it! The application will start and you can begin exploring multi-agent simulations.

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

The simplest way to install Swarm Squad is directly from PyPI:

```bash
# Install the package using uv
uv pip install swarm-squad
```

### Option 2: Development Installation

For contributors, developers, or if you plan to modify the framework:

**Additional Prerequisites for Development:**

- **[git](https://git-scm.com/downloads)**: For cloning the repository
- **[ruff](https://docs.astral.sh/ruff/)**: For code linting and formatting
- **[pre-commit](https://pre-commit.com/)**: For code quality hooks

```bash
# Clone the repository
git clone https://github.com/Sang-Buster/Swarm-Squad
cd Swarm-Squad

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

## Running Swarm Squad

After installation, you can run Swarm Squad using the command-line interface:

```bash
# Run with default settings
swarm-squad

# Show available options and help
swarm-squad --help
```

## Environment Configuration (Optional)

For advanced features, you can configure some environment variables:

```bash
# Copy the example environment file (only if cloned from source)
cp .env.example .env
```

Edit the `.env` file and configure the following variables:

- **`MAPBOX_ACCESS_TOKEN`**: Required for map visualization features
  - Sign up at [https://www.mapbox.com/](https://www.mapbox.com/) to get your access token
- **`OLLAMA_API_URL`**: URL for Ollama API integration
  - Update if your Ollama instance is running on a different address
- **`DATABASE_PATH`**: Path to the database file
  - Specify if you want to use a custom database file location

## Development Setup

If you're planning to develop or extend Swarm Squad, set up the development environment:

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
uv run src/swarm_squad/app.py
```

## Project Structure

Understanding the Swarm Squad file structure will help you navigate and extend the framework:

```
📂 Swarm Squad
┣ 📂 src/swarm_squad/          # Main source code
┃ ┣ 📂 assets/                 # Static assets (CSS, JS, images)
┃ ┃ ┣ 📂 css/                  # Stylesheets
┃ ┃ ┣ 📂 js/                   # JavaScript files
┃ ┃ ┣ 📂 models/               # 3D models and assets
┃ ┃ ┗ 📂 screenshots/          # Application screenshots
┃ ┣ 📂 cli/                    # Command-line interface
┃ ┣ 📂 components/             # Reusable UI components
┃ ┣ 📂 data/                   # Database and data files
┃ ┣ 📂 pages/                  # Page components and routing
┃ ┣ 📂 scripts/                # Simulation and algorithm scripts
┃ ┣ 📂 utils/                  # Utility functions and helpers
┃ ┣ 📄 app.py                  # Main application entry point
┃ ┗ 📄 core.py                 # Core Dash application logic
┣ 📄 .env.example              # Environment variables template
┣ 📄 pyproject.toml            # Project configuration
┗ 📄 uv.lock                   # Dependency lock file
```

## First Simulation

Once you have Swarm Squad installed and configured, you can run your first simulation:

1. **Launch the Application**:

   ```bash
   swarm-squad
   ```

2. **Access the Web Interface**: Open your browser and navigate to the URL displayed in the terminal (typically `http://localhost:8050`)

3. **Explore the Interface**: The web interface provides:
   - Real-time simulation visualization
   - Agent behavior configuration
   - Environment setup tools
   - Performance analytics dashboard

## Next Steps

Now that you have Swarm Squad installed and running, explore these areas:

1. **[Architecture](./architecture.md)**: Understand the framework's design and components
2. **[Configuration](./configuration.md)**: Learn about customization options and settings
3. **[Demo](./demo.md)**: Try out example simulations and use cases
4. **Community**: Join the Swarm Squad community for support and collaboration

## Troubleshooting

If you encounter issues during installation or setup:

### Common Issues

- **Python Version**: Ensure you're using Python 3.10 or higher
- **Virtual Environment**: Always work within a virtual environment to avoid conflicts
- **Dependencies**: Run `uv pip install -e .` again if you encounter import errors
- **Environment Variables**: Verify that all required environment variables are set correctly

### Getting Help

- Check the error messages for specific guidance
- Review the logs in the terminal output
- Ensure all prerequisites are correctly installed
- Visit the project's GitHub repository for issue tracking and community support

With Swarm Squad properly installed and configured, you're ready to explore the powerful world of multi-agent simulation!
