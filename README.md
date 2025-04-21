<div align="center">
<img src="./docs/public/favicon.ico" width=20% alt="logo">
<h1 align>Swarm-Squad | Doc</h1>
</div>

## ⚙️ Prerequisites

- Node.js (v22 or higher)
- npm

## 🛠️ Project Setup

We recommend using Node Version Manager (NVM) to install Node.js:

1. **Install NVM:**

   ```bash
   curl -o- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.2/install.sh | bash
   ```

   or

   ```bash
   wget -qO- https://raw.githubusercontent.com/nvm-sh/nvm/v0.40.2/install.sh | bash
   ```

2. **Install Node.js:**

   ```bash
   nvm install 22
   nvm use 22
   ```

3. **Verify installation:**
   ```bash
   node --version
   npm --version
   ```

## 🚀 Getting Started

1. **Clone the repository:**

   ```bash
   git clone https://github.com/Swarm-Squad/Docs.git
   cd Docs
   ```

2. **Install dependencies:**

   ```bash
   npm install
   ```

3. **Run the development server:**

   ```bash
   npm run docs:dev
   ```

4. **Building for Production:**

   ```bash
   npm run docs:build
   ```

5. **Preview Production Build:**

   ```bash
   npm run docs:preview
   ```

6. **Check formatting:**

   ```bash
   npm run format:fail
   npm run format
   ```

7. **Finalize build:**
   ```bash
   npm run check
   ```
