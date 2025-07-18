# Run commands to install needed json packages.
```bash
nvm ls                  # 
nvm use node 19.4
npm install
npm run dev
```

# API Node Setup

This guide explains how to set up and run the Node.js API for this project.

## Prerequisites

- [NVM (Node Version Manager)](https://github.com/nvm-sh/nvm) installed
- Node.js v19.4 installed via NVM

## Setup Steps

1. **List installed Node.js versions:**
   ```bash
   nvm ls
   ```

2. **Switch to Node.js v19.4:**
   ```bash
   nvm use 19.4
   ```

3. **Install dependencies listed in package.json file:**
   ```bash
   npm install
   ```

4. **Start the development server:**
   ```bash
   npm run dev
   ```

The API will now run in development mode.
