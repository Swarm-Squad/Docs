---
outline: deep
---

# Getting Started with Swarm Squad Episode II

Welcome to Swarm Squad Episode II: The Digital Dialogue, a modern multi-agent system framework featuring real-time communication, enhanced user interfaces, and advanced chatbot capabilities for seamless human-AI collaboration.

## What is Swarm Squad Episode II?

Swarm Squad Episode II is an advanced simulation framework that extends the Swarm Squad ecosystem with modern web technologies and real-time communication capabilities. The framework features:

- 💬 **Real-time Communication**: WebSocket-based messaging for instant agent interactions
- 🌐 **Modern Web Interface**: Built with Next.js, TypeScript, and Tailwind CSS
- 🤖 **Enhanced Chatbot Integration**: Advanced AI-powered chat capabilities
- 🚀 **Full-stack Architecture**: Separate frontend and backend for scalability
- 📊 **Interactive Dashboards**: Real-time visualization and monitoring
- 🔄 **Live Updates**: Real-time data synchronization across all components
- 🎯 **User-Centric Design**: Intuitive interface for seamless user experience
- 🛠️ **Developer-Friendly**: Comprehensive CLI tools and development utilities

## Quick Start

For most users, getting started with Swarm Squad Episode II is as simple as:

```bash
# Install Swarm Squad Episode II
uv pip install swarm-squad-ep2

# Launch the application
swarm-squad-ep2
swarm-squad-ep2 --help
```

That's it! The application will start both the backend and frontend, and you can begin exploring modern multi-agent systems.

## Prerequisites

For basic usage, you only need:

- **[uv](https://docs.astral.sh/uv/getting-started/installation/)**: For package installation and management (recommended)

### Installing uv

```bash
# macOS/Linux
curl -LsSf https://astral.sh/uv/install.sh | sh

# Windows
powershell -c "irm https://astral.sh/uv/install.ps1 | iex"
```

## Installation

### Option 1: Install from PyPI (Recommended)

The simplest way to install Swarm Squad Episode II is directly from PyPI:

```bash
# Install the package using uv
uv pip install swarm-squad-ep2
```

### Option 2: Development Installation

For contributors, developers, or if you want to modify the framework:

**Additional Prerequisites for Development:**

- **Node.js v18 or higher**: For the frontend application (recommended: install via [nvm](https://github.com/nvm-sh/nvm))
- **[pnpm](https://pnpm.io/installation)**: For Node.js frontend dependencies (recommended)
- **[git](https://git-scm.com/downloads)**: For cloning the repository

#### Install Node.js and pnpm for Development

```bash
# Install nvm (Node Version Manager)
curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.0/install.sh | bash

# Install and use Node.js 18
nvm install 18
nvm use 18

# Install pnpm globally
npm install -g pnpm
```

#### Development Setup

```bash
# Clone the repository
git clone https://github.com/Sang-Buster/Swarm-Squad-Ep2
cd Swarm-Squad-Ep2

# Create and activate virtual environment
uv venv --python 3.10
source .venv/bin/activate  # On Linux/macOS
# Or: .venv\Scripts\activate  # On Windows

# Install in development mode
uv pip install -e .
```

## Running Swarm Squad Episode II

### Using the CLI Interface

After installation, you can use the comprehensive CLI interface:

```bash
# Show all available commands
swarm-squad-ep2 --help
```

### Available Commands

#### Launch Complete Application

```bash
# Launch both backend and frontend together
swarm-squad-ep2 launch
```

#### Run Components Individually

```bash
# Run FastAPI backend server (default port 8000)
swarm-squad-ep2 fastapi

# Run FastAPI backend on custom port
swarm-squad-ep2 fastapi --port 8080

# Run Next.js frontend (default port 3000)
swarm-squad-ep2 webui

# Run frontend on custom port
swarm-squad-ep2 webui --port 3001
```

#### Development and Setup Commands

```bash
# Install frontend dependencies (development only)
swarm-squad-ep2 install

# Build frontend for production (development only)
swarm-squad-ep2 build

# Run vehicle simulation components
swarm-squad-ep2 setup

# Run with matplotlib visualization
swarm-squad-ep2 setup visualize

# Run WebSocket test client
swarm-squad-ep2 setup test
```

## Development Setup

If you're planning to develop or extend Swarm Squad Episode II:

### Install Development Dependencies

```bash
# Install development dependencies
uv pip install -e .
```

### Development Workflow

```bash
# Install frontend dependencies for development
swarm-squad-ep2 install

# Build frontend for production
swarm-squad-ep2 build

# Launch the complete application
swarm-squad-ep2 launch
```

## Project Structure

Understanding the Swarm Squad Episode II file structure will help you navigate and extend the framework:

```
📂 Swarm Squad Episode II
┣ 📂 frontend/                 # Next.js React application
┃ ┣ 📂 src/                    # Source code
┃ ┃ ┣ 📂 components/           # React components
┃ ┃ ┣ 📂 pages/                # Next.js pages
┃ ┃ ┣ 📂 styles/               # CSS and styling
┃ ┃ ┣ 📂 utils/                # Utility functions
┃ ┃ ┗ 📂 hooks/                # Custom React hooks
┃ ┣ 📄 package.json            # Frontend dependencies
┃ ┣ 📄 tailwind.config.js      # Tailwind CSS configuration
┃ ┗ 📄 next.config.js          # Next.js configuration
┣ 📂 backend/                  # FastAPI Python application
┃ ┣ 📂 fastapi/                # FastAPI application
┃ ┃ ┣ 📂 routers/              # API route handlers
┃ ┃ ┣ 📂 models/               # Data models
┃ ┃ ┣ 📂 services/             # Business logic
┃ ┃ ┗ 📄 main.py               # FastAPI application entry point
┃ ┣ 📂 scripts/                # Utility scripts
┃ ┗ 📄 requirements.txt        # Python dependencies
┣ 📂 src/swarm_squad_ep2/      # Core package
┃ ┣ 📂 cli/                    # Command-line interface
┃ ┗ 📄 __init__.py             # Package initialization
┣ 📄 pyproject.toml            # Python project configuration
┗ 📄 uv.lock                   # Dependency lock file
```

## Key Components

Swarm Squad Episode II includes several modern components for enhanced user experience:

### Frontend Architecture

- **Next.js Framework**: Server-side rendering and modern React features
- **TypeScript**: Type-safe development for better code quality
- **Tailwind CSS**: Utility-first styling for responsive design
- **Real-time Communication**: WebSocket integration for live updates

### Backend Architecture

- **FastAPI**: High-performance Python web framework
- **WebSocket Support**: Real-time bidirectional communication
- **RESTful API**: Standard HTTP endpoints for data operations
- **Integration Layer**: Connects to Swarm Squad simulation engine

### CLI Tools

The CLI provides comprehensive commands for different workflows:

- **`launch`**: Complete application startup
- **`fastapi`**: Backend server management
- **`webui`**: Frontend development server
- **`setup`**: Vehicle simulation and testing
- **`install`**: Development dependency management
- **`build`**: Production build process

## First Application Launch

Once you have Swarm Squad Episode II installed, you can launch your first session:

1. **Launch the Application**:

   ```bash
   swarm-squad-ep2 launch
   ```

2. **Access the Web Interface**: Open your browser and navigate to `http://localhost:3000`

3. **Explore the Features**:

   - User authentication and account management
   - Real-time chat interface
   - Interactive dashboards
   - Live data visualization
   - WebSocket communication status

4. **Test the API**: The backend API documentation is available at `http://localhost:8000/docs`

## Vehicle Simulation

Swarm Squad Episode II includes vehicle simulation capabilities:

```bash
# Run basic vehicle simulation
swarm-squad-ep2 setup

# Run simulation with matplotlib visualization
swarm-squad-ep2 setup visualize

# Test WebSocket connections
swarm-squad-ep2 setup test
```

## Configuration

The application behavior can be configured through various methods:

- **Environment Variables**: Set in `.env` files for both frontend and backend
- **Configuration Files**: Modify settings in respective config files
- **CLI Parameters**: Pass options like `--port` to customize server settings
- **Runtime Settings**: Adjust settings through the web interface

## Next Steps

Now that you have Swarm Squad Episode II installed and running, explore these areas:

1. **[Architecture](./architecture.md)**: Understand the full-stack system design
2. **[Configuration](./configuration.md)**: Learn about customization options and settings
3. **[Demo](./demo.md)**: Try out example scenarios and use cases
4. **API Documentation**: Explore the backend API at `http://localhost:8000/docs`
5. **Community**: Join the Swarm Squad community for support and collaboration

## Troubleshooting

If you encounter issues during installation or setup:

### Common Issues

- **Python Version**: Ensure you're using Python 3.10 or higher
- **Port Conflicts**: Check if ports 3000 and 8000 are available, or use custom ports
- **Dependencies**: Run `uv pip install -e .` again if you encounter import errors
- **WebSocket Issues**: Ensure WebSocket connections are not blocked by firewalls

### Getting Help

- Check the error messages for specific guidance
- Review the logs in the terminal output
- Ensure all prerequisites are correctly installed
- Use `swarm-squad-ep2 --help` to see all available commands
- Visit the project's GitHub repository for issue tracking and community support

### Development Issues

- Use `swarm-squad-ep2 install` to ensure frontend dependencies are installed
- Use `swarm-squad-ep2 build` to create production builds
- Verify that both frontend and backend are running properly
- Check the browser console for frontend errors

With Swarm Squad Episode II properly installed and configured, you're ready to explore modern multi-agent systems with real-time communication and enhanced user interfaces!
