# Node-RED Team Project Template

This repository provides a basic setup for collaborating on a Node-RED project with Git.

## Getting Started

1. **Clone the repository**
   ```bash
   git clone <repo-url>
   cd <repo>
   ```
2. **Install dependencies**
   ```bash
   npm install
   ```
3. **Create your environment configuration**
   ```bash
   cp .env.example .env
   # edit .env with your values
   ```
4. **Start Node-RED**
   ```bash
   npm start
   ```

## Deployment

### Manual

On the server:
```bash
git pull
npm install
# restart Node-RED service
systemctl restart nodered
```

### GitHub Actions (optional)

A simple workflow is provided in `.github/workflows/deploy.yml`. It pulls the latest code on your server when you push to `main`. Configure the required deployment secrets before enabling it.
