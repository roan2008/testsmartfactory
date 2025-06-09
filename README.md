# Node-RED Smart Factory Project

This repository contains a Node-RED project for smart factory automation with example flows for testing and development.

## Features

- Basic "Hello World" flow for testing
- File logging capability
- Environment configuration support
- GitHub Actions deployment workflow

## Getting Started

1. **Clone the repository**
   ```bash
   git clone <repo-url>
   cd testsmartfactory
   ```

2. **Install dependencies**
   ```bash
   npm install
   ```

3. **Create your environment configuration**
   ```bash
   cp .env.example .env
   # Edit .env with your values (username, password, port)
   ```

4. **Start Node-RED**
   ```bash
   npm start
   # or
   npx node-red --userDir . --flowFile flows.json
   ```

5. **Access Node-RED Editor**
   Open your browser and go to: http://localhost:1880

## Project Structure

- `flows.json` - Main Node-RED flows
- `package.json` - Node.js dependencies
- `.env.example` - Environment variables template
- `settings.js` - Node-RED configuration
- `.github/workflows/deploy.yml` - CI/CD configuration

## Example Flows

The project includes:
- **Inject → Debug**: Basic message flow with 1-minute timer
- **Manual Hello → Function → File**: Manual trigger that writes formatted messages to a file

## Security Notes

- Never commit credentials files (`*_cred.json`)
- Use environment variables for sensitive data
- Review `settings.js` before deployment

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
