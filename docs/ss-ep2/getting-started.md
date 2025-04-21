---
outline: deep
---

# Getting Started with Swarm Squad Episode II

This guide will help you set up and run Swarm Squad Episode II: The Digital Dialogue, focusing on real-time communication and enhanced user interfaces for multi-agent systems.

## Prerequisites

Before installing Swarm Squad Episode II, ensure you have:

- **Node.js**: v18 or higher (recommended: install via [nvm](https://github.com/nvm-sh/nvm))
- **Package Managers**:
  - [pnpm](https://pnpm.io/installation): For frontend dependencies
  - [uv](https://docs.astral.sh/uv/getting-started/installation/) for Python environment and dependency management
- [git](https://git-scm.com/downloads) (for cloning the repository if installing from source)

## Installation

### Comprehensive Setup

The easiest way to set up the complete environment is using the provided Makefile:

```bash
# Clone the repository
git clone https://github.com/Sang-Buster/Swarm-Squad-Ep2
cd Swarm-Squad-Ep2

# Install all dependencies (frontend, backend, and pre-commit hooks)
make install
```

### Manual Setup

If you prefer to install components individually:

#### 1. Install Frontend Dependencies

```bash
cd frontend
pnpm install
```

#### 2. Install Backend Dependencies

```bash
cd backend
uv venv
source .venv/bin/activate  # On Linux/macOS
# Or: .venv\Scripts\activate  # On Windows
uv pip install -r requirements.txt
```

#### 3. Install Pre-commit Hooks (Optional)

```bash
uv pip install pre-commit
pre-commit install --hook-type commit-msg --hook-type pre-commit --hook-type pre-push
```

## Running the Application

### Using Makefile

The simplest way to run the complete application:

```bash
# Start both frontend and backend
make dev

# Or start components individually
make frontend  # Start only frontend
make backend   # Start only backend
```

### Manual Startup

If you're not using the Makefile:

#### Frontend

```bash
cd frontend
pnpm dev
```

The frontend will be available at `http://localhost:3000`

#### Backend

```bash
cd backend
source .venv/bin/activate  # On Linux/macOS
# Or: .venv\Scripts\activate  # On Windows
uvicorn fastapi.main:app --reload
```

The backend API will be available at `http://localhost:8000`

## Development Workflow

### Code Quality Tools

```bash
# Run all code quality checks
make lint

# Or run them individually
make lint-frontend  # Lint and format frontend code
make lint-backend   # Lint and format backend code

# Clean up running processes
make clean
```

### Project Structure

Swarm Squad Episode II is organized into two main components:

- **Frontend**: Located in the `frontend` directory

  - Built with Next.js, TypeScript, and Tailwind CSS
  - Provides the user interface and chat functionality
  - Communicates with the backend via API and WebSockets

- **Backend**: Located in the `backend` directory
  - FastAPI application providing API endpoints and WebSocket communication
  - Integration with simulation scripts and utilities
  - Connects to the Swarm Squad simulation engine

## Next Steps

Now that you have Swarm Squad Episode II running, you might want to:

1. Create a user account and log in to the system
2. Explore the chat interface and real-time communication features
3. Review the [Architecture](./architecture.md) documentation
4. Learn about the [Configuration](./configuration.md) options for customizing your setup

## Troubleshooting

If you encounter any issues:

- Ensure all prerequisites are correctly installed
- Verify that both frontend and backend are running
- Check console outputs for error messages
- Make sure WebSocket connections are not blocked by firewalls
- For development issues, ensure all code quality checks pass before committing
