<div align="center">
<img src="https://github.com/Swarm-Squad/Docs/raw/refs/heads/main/docs/public/favicon.ico" width=20% alt="logo">
<h1 align>Swarm-Squad | Doc</h1>
</div>

## 🚀 Getting Started

### ⚙️ Prerequisites

- Node.js (v22 or higher)
- npm

### 📥 Installing Node.js with NVM

We recommend using Node Version Manager (NVM) to install Node.js:

1. Install NVM:
   ```bash
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
   ```
   or
   ```bash
   wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.39.3/install.sh | bash
   ```

2. Install Node.js:
   ```bash
   nvm install 22
   nvm use 22
   ```

3. Verify installation:
   ```bash
   node --version
   npm --version
   ```

### 🛠️ Setting Up Documentation

1. Clone the repository:
   ```bash
   git clone https://github.com/Swarm-Squad/Docs.git
   cd Docs
   ```

2. Install dependencies:
   ```bash
   npm install
   ```

3. Run the development server:
   ```bash
   npm run dev
   ```
   This will start a local server at http://localhost:5173

### 📦 Building for Production

To build the documentation for production:

```bash
npm run build
```

The built files will be available in the `docs/.vitepress/dist` directory.

### 🔍 Preview Production Build

To preview the production build locally:

```bash
npm run preview
```